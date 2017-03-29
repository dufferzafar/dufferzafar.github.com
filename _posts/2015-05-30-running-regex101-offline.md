---
layout: post
title: "Running Regex101 Offline"
date: 2015-05-30 03:23:19 +0530
---

I was working on something when I suddenly needed some regex-fu. I opened a new browser tab, typed `regex101` and pressed enter, and then I realized, I am at a place where sites usually take five fucking minutes to load up.

We need to improvise, I thought.

<!-- more -->

I needed something that could work offline. I googled around (which took ages) to find an offline tool, but none of the results impressed me, and then I found [this](https://github.com/Syskaw/Regex101.com-offline-app/) - a way of getting regex101 itself working offline.

Turns out, some wget magic is all that we needed.

Cloning the site locally took around 10 minutes:

```bash
mkdir ~/regex101
cd ~/regex101
wget -r --no-host-directories --no-parent http://regex101.com
wget --output-document ./js/javascript.regex101.js http://regex101.com/js/javascript.regex101.js;
wget --output-document ./js/pcre.regex101.js http://regex101.com/js/pcre.regex101.js;
wget --output-document ./js/pcrelib16.js http://regex101.com/js/pcrelib16.js;
```

I used python's http.server module to host the site:

`python3 -m http.server 8090`

The site loaded, but a few things were still out of place, like it still tried fetching jquery, font awesome, a font from google fonts etc.

I then manually fetched each and every dependency, and edited the index.html to use the local ones. 

Thirty minutes later I had a fully offline version up and running.

But we're not done yet.

I am not gonna `cd` into some directory and run `python3 -m http.server 8090` everytime I need regexes. 

We need to improvise.

Thanks to Linux Utility Lab, I learnt how to host sites using Apache this semester. I already had apache2 installed. The rest was easy:

Create a directory that will host all the files: 
`sudo mkdir -p /var/www/101regex.com`

Put all the site required files there: 
`sudo cp -r ~/regex101 /var/www/101regex.com`. 

Here's a [ZIP of files](https://www.dropbox.com/s/r0gguscne28bf34/Regex101-30-May-2015.zip?dl=0) that you can use.

Create a site configuration:

Copy default: 
`sudo cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/101regex.com.conf`

Vim-it: `sudo vim /etc/apache2/sites-available/101regex.com.conf`

Here's how my config looked:

```
<VirtualHost *:80>
  ServerName 101regex.com
  ServerAlias www.101regex.com

  ServerAdmin admin@101regex.com
  DocumentRoot /var/www/101regex.com
</VirtualHost>
```

Now edit the hosts file to have a working url: 

Open: `sudo vim /etc/hosts`

Add line: `127.0.0.1  101regex.com`

Enable the site, and restart the server.

`sudo a2ensite 101regex.com.conf`

`sudo service apache2 restart`

I now have a fully functional Regex101 running locally at: `101regex.com`

![Regex101 Working Offline](/images/regex101-offline.png)

I don't even remeber what I wanted to do with regexes in the first place.

So, I decided to write down a blog post.

By the way, [It's Four](https://www.ted.com/talks/rives_on_4_a_m?language=en) [In The Morning](https://www.ted.com/talks/rives_a_museum_of_4_o_clock_in_the_morning?language=en).

**Update:**

4:19 AM

Ugh!

This post was supposed to end here, and I was supposed to be sleeping by now, but Octopress decided to go haywire on me - some segmentation fault while running `rake generate`. 

I've found this [gist](https://gist.github.com/imathis/1104557) that will probably resolve the issue, but the problem is, a lot of packages will need to be downloaded for that. :/

4:40 AM

This is taking too much time, I guess I'll have to continue later.

7:41 PM

After installing the wrong version of ruby twice, then getting rvm to play nicely with zsh, and upgrading the rubies, everythin was finally working.

Maybe this is an indication that I'm using the wrong toolchain, and should just move the blog to Python. Another time, I guess.
