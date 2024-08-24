Tweetstorm: The Curious case of PDF titles.

Featuring an interesting problem, a hacky solution, my weird workflow, someone's cancelled credit card, and an #xkcd reference.

What more could you want?

1/n

---

PDFs downloaded from the web usually have names like "gfs-sosp2003.pdf"  How do you rename them to: "Google File System - 2003.pdf"?

Some files have a "title" metadata field, containing the right thing.

So we could create a script that uses that field's info to rename files. 

---

But what if there is no such field? Or what if that field contains something like "paper.dvi"? (as is very common.)

If you were to actually open the PDF, it wouldn't take you very long to figure out what the title is - something in bold that stands out from other text.

---

If the title is supposed to visually stand out, you could write code that detects exactly that.

Actually *you* don't even have to write it. Folks at #KDE have already done that: https://github.com/KDE/kfilemetadata/blob/621101fd9e9d82be3d84f2140a4bf53ea13fd3f0/src/extractors/popplerextractor.cpp#L107

It uses heuristics that try to guess the title and it works reasonably well.

---

I wrote a script around this that actually does the renaming: https://github.com/dufferzafar/.scripts/blob/master/pdf-titles

Tiny caveat though: You can only use the script if you compile an executable fro the KFileMetadata library.

I wrote this script around an year ago and really like it.

But...

---

Around the same time in 2017, a guy had to cancel his credit card because of the exact same title parsing C++ code!

Here's his story: https://blog.flameeyes.eu/2017/09/how-i-leaked-my-own-credit-card-number/

Read it, I'll wait!

---

The guy actually went ahead and got that code removed from the #KDE library: https://phabricator.kde.org/D8007

And nobody really objected.

---

It's funny how people can have such different experiences with the same code.

Reminds me of https://xkcd.com/1172/

---

Now that the code is officially dead, I'm thinking of writing the title parsing heuristics in #python itself.

But first I need to figure out which PDF library to use. pdfminer? python-poppler? pypdf? pdfreader?

