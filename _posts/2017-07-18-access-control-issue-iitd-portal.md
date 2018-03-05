---
layout: post
title:  "An access control issue in IITD's Portal"
date:   2017-07-18 7:03:48
---

<i>
I initially wrote this post, published it publicly on the blog, and later removed it when Shivam & Aditya both felt that someone from IIT might see it and penalize me. I now feel that we might be overestimating the danger and no one really cares.
</i>

This is a post on how I wrote a script that downloaded details of everyone who is in my MTech Batch. 

I was able to do this because of an access control vulnerability on one of IITD's portals that allows people to see files that don't belong to them. This is similar to what [weev](https://en.wikipedia.org/wiki/Weev) went to jail for, except I don't plan on making the data public (more than it already is.)

<!-- more -->

<hr><br>

The portal is made for CS M.Tech students to fill a form with information like AADHAAR number, Blood group etc.

While checking the generated PDF output I noticed that the PDF URL had my entry number and it occurred to me that maybe, just maybe, I could access details of others. If only I knew their entry number.

The thing about numbers is, there's always the next one.

So I entered a number that was closer to mine and sure enough, I could see all their details.

Hm, I thought, we can surely automate this.
<br><br><br>


I fire up my Sublime, open a new tab, go into distraction free mode and start typing.

And the very first thing I typed made me chuckle: `import python` 

I'm not shitting you! I have no idea why but I actually typed that and only noticed it when I ran the script later and it err'ed. [Am I getting old already?]

The next I thing I wrote was correct though: `import request`. That is how you web in Python.

And then I stopped. To think.

So we want to download PDFs via requests right, that's easy. 

Just [google "python requests download pdf"](http://lmgtfy.com/?q=python requests download pdf) and [feel lucky](https://stackoverflow.com/questions/34503412/). The code turned out to be quite obvious. You just have to open a file and write the contents. This made me feel bad for not being able to type it out from memory.


I split out the URL and filename part, so here's what we have till now:

```py
ROOT_URL = "https://portal/uploads/"
FILE_PATTERN = "2017MCS%d.pdf"

# 2076 is my number
for entry_number in [2076]:

    filename = FILE_PATTERN % entry_number
    resp = requests.get(ROOT_URL + filename)

    with open(filename, "wb") as pdf:
        pdf.write(resp.content)
```

Hey, let's put these files into a separate directory. 

I knew the snippet as I've done this a lot:

```py
import os
ROOT_DIR = os.path.expanduser("~/Downloads/IIT-D")

filepath = os.path.join(ROOT_DIR, filename)

# Then use this filepath instead of filename 
# as a parameter to open()
```

Now, that directory didn't actually exist and this'll fail if it doesn't. I could've just created that folder manually by opening my file manager and doing it like I always do but I knew the snippet for this too:

```py
if not os.path.exists(ROOT_DIR):
    os.mkdir(ROOT_DIR)
```

[I always forget if it is `makedir` or `mkdir` but Sublime's Autocomplete has my back.]

The script looked worth running at this point, so I saved it and ran!

The first error was silly. `No module named request`. wtf. I'm pretty sure I have it. It later realized that the module is called `requests` and not `request`. whatever man. 

Fix it. Re-run. 

The next one looked like a real error, mostly because it mentioned `SSL certificates`. 

The error, like most errors, was incomprehensible but I recognized it as the same one that occurred in one of [my other scripts](https://github.com/dufferzafar/.scripts/blob/master/mts) a few days ago. I was too busy doing something else that day. But not today man, not today.

So what do I do when I'm having SSL errors? I try plain old HTTP ofcourse. It's `https` that's giving me troubles, right?

I dropped the `s` and tried again. No errors, but the request 404'ed. 

Something really is broken.

<br><br>

Then it occurred to me - this wasn't working because the PDF files are not publicly accessible, but behind a login-wall and logging in won't be easy because that page has a CAPTCHA on it.

Damn. [This escalated quickly.](https://xkcd.com/1425/)

<br><br>

Before I could google "python breaking captcha", I had another insight - I don't have to login!

I'm already logged in on my browser so I can just use those cookies in my script. 

Now there are a lot of ways the cookies can be exported (via extensions etc.) but I used something I've relied on before - the "Networks" tab of the browser's devtools.

I copied the browser request to the PDF as a CURL command which looked like this: 

```bash
curl 'https://portal/uploads/2017MCS2076.pdf' -H 'Host: portal.in' 
-H 'User-Agent: Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:54.0) Gecko/20100101 Firefox/54.0' 
-H 'Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8' -H 'Accept-Language: en-US,en;q=0.5' 
--compressed -H 'Cookie: SESS1dragonstone=aryarocks; PHPSESSID=jonsnowacchabacchahai' 
-H 'Connection: keep-alive' -H 'Upgrade-Insecure-Requests: 1'
```

It may look ugly, but this little one-liner gets me out of the browser and I can now test things on the shell. 

So I ran the command but CURL threw an error - something about SSL certificates being invalid or some such. BUT, curl being the good guy it is, mentioned I could disable these verifications by passing in the `-k` parameter. 

So I tried that and it started throwing some binary shit on my screen. No errors though. 

It took to me a moment to realise that this is what PDF files actually look like. 

Things were working now!

<br><br>

The curl command just proved I was going in the right direction but we still need everything in Python and to do the conversion I used [this tool](https://curl.trillworks.com/) which was already in my browser's history. You just paste the command and get python code. Simple enough!

Since we only need the cookies (not headers) and the requests call needs to know about them. This is the code that results:

```py
cookies = {
    'SESS1dragonstone': 'aryarocks',
    'PHPSESSID': 'jonsnowacchabacchahai',
}

resp = requests.get(..., cookies=cookies)
```

I made these changes and ran the script. It threw the SSL error too. This was expected though. 

We just need to find out what the `-k` switch is called in requests. So a quick [google for "python requests disable ssl"](http://lmgtfy.com/?q=python requests disable ssl) had me [set](https://stackoverflow.com/questions/34503206). We just need a `verify=False` in our requests call.

Edit+Run again and it worked - I had my PDF file in that directory!

FINALLLY!

<br><br>

requests was still throwing some boring SSL warning though, so it took me another [google](http://lmgtfy.com/?q=disable requests warning) and [SO link](
https://stackoverflow.com/questions/15445981) to get this ugly two-liner:

```py
from requests.packages.urllib3.exceptions import InsecureRequestWarning
requests.packages.urllib3.disable_warnings(InsecureRequestWarning)
```

Re-ran the script and ensured everything is smoooth. 

<br><br>

So I can download my PDF file now. We just have to download all the others!

Well that's easy, I'll just use a `range(2060, 2080)` in my for loop. But what if that number does not exist? More code:

```py
if not resp.ok:
    print(" Not Exists: " + filename)
    continue
```

Running the code for (2060,2080) resulted in 8 PDF files! 

Things were working well now. Which made me a bit cautious and I got worried about how I was making too many requests successively and decided to wait for a few seconds before making the next call. We don't want to raise any alarms, do we!

Now I knew this could be done via `time.sleep` but who remembers whether the argument is seconds or milliseconds. Another [google ("python time sleep")](http://lmgtfy.com/?q=python time sleep) and [seconds it is](https://stackoverflow.com/questions/510348/).

I also added this bit which prevents re-downloading of files:

```py
if os.path.exists(filepath):
    print("Already Exists: " + filename)
    continue
```

After this, I just played out with the range a bit, making small increments each time until I reached a number beyond which all requests 404'ed.

<br><br>

I finally had the 26 files I wanted.

I went through a few of them and it turned out (as it often does) that I just wasn't interested in the output. It was the process and the code that mattered to me.

I still did read those files though, and while I was going through one them I thought, man wouldn't it be nice to have all this data as a CSV - a line per student.

But hey, we can automate that!

<hr>
<br>

<i>
I wrote this post and showed it to Aditya. We were discussing how serious this is when he sent me a URL: https://portal/uploads/
</i>

<i>
It turns out that there is a folder on the portal that has ALL the files of everyone (not just MTech) who registered in 2017 along with passport size photographs of people who registered in 2016.
</i>

<i>
And the best part - you don't require any login. 
</i>

<i>
I could just give you the URL and you'll have have AADHAAR and PAN details of students and their parents, but who cares right?
</i>
