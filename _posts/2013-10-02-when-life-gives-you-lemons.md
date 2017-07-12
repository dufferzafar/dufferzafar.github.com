---
layout: post
title: "When life gives you lemons..."
date: 2013-10-02 10:12
---

I messed up really big time the day before yesterday. I was working on Cryptex - a hacking challenge sort-of thing. I don't exactly remember what I was doing, maybe renaming some files... when I saw a folder that shouldn't have been there, so I did what I always do - press Shift+Delete followed by Enter.

<!-- more -->

A moment later I started yelling - fuck! fuck! shit! - I said some not-so-decent things in Hindi too but let's not get into that detail. Turns out, I deleted the entire Cryptex root folder. Everything related to the project Gone.

Thankfully the code was also stored on Github but I had not pushed my most recent local changes - the ones I was working on. Hard Luck.

The first thing that came to my mind as I sat down for damage control was the fact that files are never actually deleted (If you think I'm crazy, read [this](http://www.howtogeek.com/125521/htg-explains-why-deleted-files-can-be-recovered-and-how-you-can-prevent-it/).) It's all there on the hard drive, so I could just bring it all back (in theory.) I started Recuva - a free tool to recover deleted data. It took about a minute to find tonnes of deleted shit on my "C:" drive but sadly, and not surprisingly, the files I needed weren't listed. Welcome to the real world.

Recuva also provides an option to Deep scan your drives but I've used that stuff before -- It'd have taken about an hour to find the files and the chances of recovery would still have been feeble.

So, having nothing left to try, I synced the folder with Github but it was about a day old and everything I had done in the past twenty hours was gone. Shit Happens. It's like clearing some checkpoints and then forgetting to save the game. Now you'll have to replay the levels and so I did...

I did everything all over again -- wrote the code, renamed the files, some more shit. It turned out to be fairly okay if you ask me.

But now, as I am writing this, I'm really glad that it all happened because -

A. I got to write this blog post, I love writing and all I need is a topic I sincerely care about.

B. I thought of a nifty bug in the code I was writing -- had something to do with disabled javascript in the user's browser.

C. Most importantly, I learnt the importance of backups and why they are as essential as everybody claims them to be. So I decided that I'd backup my stuff too. But come on, you don't expect me to copy folders to some other place every time I update something. Nope, I am gonna write a script to do that.

I have figured out all the internals. I'll code it in AHK (duh!) and it'll be timer based -- backups will be made every fifteen minutes or so. I am going to use 7zip to compress the folder and copy it to some place that I don't normally visit (what if I end up deleting the backups too? *shudder*)

The script will maintain at least 5 different snapshots and would delete the older one as soon as the new one comes in. I'll start by adding the core functionality first to get stuff working and would then work on additional features. It sounds fairly simple on paper. Let's see how it turns out...

> I believe when life gives you lemons, you should make lemonade...and try to find someone whose life has given them vodka, and have a party.
