---
layout: post
title:  Second Semester at IIT Delhi
date:   2018-05-18 22:46:27
---

This is episode two of my life as an M.Tech (CS) student at IIT D; [here is the first.](http://dufferzafar.github.io/2017/12/02/first-semester-iit-delhi/)

I wanted to write this post before the results were announced, but procrastination coupled with some odd work here & there prevented me from doing it. Now that the results have been declared and they turned out to be way better than I'd expected, I feel I'll be a bit biased while looking at the past. I'll try to keep this in mind.

This was a very hectic semester; even though all of them are supposed to have the same number of working days, this one felt way longer than the last, primarily because my classes aligned in a way that forced me to go to college every single day (as opposed to only around 3-days-a-week last sem.) Then there were Tuesdays, when I had one class from 11am-12 noon and the next one from 6pm-7pm, requiring me to while away 6 hours - which may not sound like much but keep in mind that there's only so many HN, Reddit, GitHub permutations possible.

I had three courses & a project this semester : 

* Network Security (SIL 765) by B. N. Jain
* [Spl. Topics in High Speed Networks - Blockchains (COL 867)](https://web.archive.org/web/20180522050229/http://www.cse.iitd.ernet.in/~vinay/courses/COL867_s18.html) by Vinay Riebero
* [Machine Learning (COL 774)](https://web.archive.org/web/20180522050126/http://www.cse.iitd.ac.in/~parags/teaching/col774/) by Parag Singla
* Minor Project under Vinay Riebero

<!-- more -->

### Network Security

I had very high hopes from this course before the semester started. I was  watching assembly tutorials in the winter break and was expecting practical security stuff - y'know, things like buffer overflows, exploit strings, and using real world tools like nmap, wireshark etc. which had already been taught in the past versions of this course in [2012-13](http://www.cse.iitd.ernet.in/~siy117527/sil765/readings.html), [2013-14](http://www.cse.iitd.ac.in/~saran/sil765/index.html) by Huzur Saran. 

Prof. Jain's version of the course turned out to be very different (& such a let down.) It was a standard crypto course - the kind that I'd already gotten bored of during B.Tech. I knew right from the first class that it'll be a dull course, but I still took it because I knew it'll be easy to score as well.

I didn't already own a security related book, so I ordered the one Prof. Jain was following - [Crypto & Network Security by William Stallings](https://www.amazon.in/Cryptography-Network-Security-Principles-Practice/dp/9332585229/). I've only read the book thrice - exactly a day before each exam (just like we used to in B.Tech) and found it to be too dry, it focusses a lot on the mechanical aspects of the algorithms and not much on high level concepts. 

To help me see the bigger picture, I watched [Christof Paar's Crypto lectures](https://www.youtube.com/channel/UC1usFRN4LCMcfIV7UjHNuQg/videos). They are quite nice once you speed them up to 2x. Sadly, he doesn't cover the application layer security portion, which I tried to cover by watching a bunch of random videos, but none of them turned out to be any good.

There were some programming assignments too: implementing DES, RSA, Timestamp Authority and a Certification Authority, all of which I did along with a [mate](https://github.com/nichit). 

You can find them on Github: [http://github.com/dufferzafar/netsec/](http://github.com/dufferzafar/netsec/)

<!-- TODO: Mention the questions he'd give for practice; papers were easy;  -->

### Spl. Topics in High Speed Networks - Blockchains

The first thing you need to know about this course is that the course code starts with an 8. I didn't know what this meant until I asked Prof. Riebero to suggest resources that weren't research papers and he said, "well, you can't avoid reading papers in an 800 level course". So yeah, that's what 800 level courses are - they contain topics that are actively being researched and usually the only reference material is a twenty-something paged paper containing all sorts of jargon; and because the Blockchain field is still nascent, the jargon itself hasn't been agreed on which makes understanding them all the more difficult. 

The course was in two main parts: 
1. Bitcoin, its peculiarities and limitations 
2. A hotchpotch of recent Blockchain-related research topics

Part one felt straightforward, because a.) the concepts were new and exciting and b.) there's a lot of [easy to digest](http://gen.lib.rus.ec/book/index.php?md5=E17DF3BD18FF91A55A2522F65EF4AD30) [reading material](http://bitcoinbook.cs.princeton.edu/) available. Part two however was tricky, mainly because the concepts got pretty esoteric pretty fast and it was hard to see the bigger picture (at first.) It also didn't help that there was no beginner friendly material available. 

To be very honest though, the papers didn't turn out to be as hard as I'd imagined. Sir had already given us a good overview of what the main idea behind each paper was and once you've read a bunch of papers from a field, you kind of develop a feel for how they're structured - so skimming becomes easier.

I found the course to be overburdening particularly because of its non-exam components - two programming assignments and a term paper:

1. A [discrete-event cryptocurrency simulator](https://github.com/dufferzafar/crypto-simulation/) - which, among other things, shows the effect that various parameters can have on a Blockchain's growth.

2. A [smart contract](https://github.com/dufferzafar/solid-media/) for a very superficial & contrived problem - which did make me learn the ethereum stack but didn't really help me appreciate what Blockchains (& Smart Contracts) are actually useful for. [^1]

3. A [paper reviewing various solutions](https://docs.google.com/document/d/1ZdxRHNJo6tP0bqWxNACbwQ1oPiG5RZqfmg0kXNCi8zE/edit?usp=sharing) to improve anonymity in cryptocurrencies.

These assignments had to be done in teams of three and I messed up by teaming with two of my seniors who later turned out to be bigger procrastinators than I am; as a result of which, I ended up doing a lot of the work alone. 

Fortunately, the hardness of the course was well balanced by an easy major exam (everything directly from notes) and easier grading.

### Machine Learning

Oh boy, I have so much to say about this, I don't even know where to begin.

I guess I'll just begin with how I didn't even want to take this course in the first place. Even though ML seems to be the jazz these days, with some cool application making the [front page of HN](http://news.ycombinator.com/) everyday, I just knew it wasn't something I wanted to do. I also didn't have the required maths background (Linear Algebra etc.) To confirm this, I had a look at some of Andrew Ng's old notes and sure enough - they looked like gibberish to me - filled with all sorts of non-ASCII symbols.

But I took the ML course anyway, perhaps because I [feared missing out](https://en.wikipedia.org/wiki/Fear_of_missing_out) - I didn't want to be the one guy who didn't understand something that was obvious to everyone else.

The course turned out to be just as I'd expected - filled with concepts that I had to learn from scratch. I didn't study from any of the oft-cited ML books, because they seem to be written for people smarter than me. What I did consult though, and ended up loving, were these books aimed at Python programmers:

["Python Data Science Handbook"](http://gen.lib.rus.ec/book/index.php?md5=0DC83AA87F6C9CBCDF330DA68412B117) - This introduces Numpy, Pandas, matplotlib libraries and then goes into machine learning algorithms - which are beautifully explained. The author is the creator of scikit-learn and knows his stuff inside out.

["Hands on Machine Learning"](http://gen.lib.rus.ec/book/index.php?md5=961B87D8FA149D92D0D3F04837EF011E) - I didn't read the Tensorflow chapters (as I used Keras & PyTorch for my assignments) but the rest of the book is pretty legit.

Apart from these, I also consumed a lot of video content (mostly during my metro commute to / from IIT.) On a typical thursday, I would watch Ng's coursera lectures in the morning while going to college; then during class, Prof. Singla would explain the same concept (sometimes in a much better way) and then on my way back I would watch Ng's stanford lectures.

The assignments are where real learning happened for me. We implemented the entire gamut of basic algorithms, from linear regression to backpropagation and in the end, had a [Kaggle competition](https://www.kaggle.com/c/col-774-spring-2018), where we played around with deep neural architectures. I know I'll forget all the mathy bits of the course before the month ends; what will stick with me, however, is just how amazing NumPy and friends are. I'd only ever heard of the "scientific Python stack", but never got around to using it till now.

As always, all my code is on Github: [https://github.com/dufferzafar/machine-learning](https://github.com/dufferzafar/machine-learning)

### Minor Project

I wanted to work on something related to "web security" but after not being able to find any professor working in that particular field, I approached Prof. Riebero because he told me that his students had worked on netsec related topics (DoS attacks, ransomwares) in the past.

Sir sent me a list of his current students and I met with a few of them but couldn't find anything interesting to work on. Still wanting to chart my own territory, I looked into a [bunch of](http://securitee.org/files/xhound-oakland17.pdf) [web security](https://www.usenix.org/system/files/conference/usenixsecurity15/sec15-paper-jagpal.pdf) [papers](https://dl.acm.org/citation.cfm?id=3137619). Even though I was familiar with the background concepts and was able to understand what problem was being solved by each paper - that wasn't enough to come up with something new to work on.

Sir then suggested to look into mobile security, because that's the only other technology with a massive reach. He'd received a fitness tracking band from a conference he went to, and wanted to look into what data those devices collected and how it could be misused. From there, we came upon [this 2017 paper](https://eprint.iacr.org/2017/1169.pdf) - which showed how accelerometer data can be used to figure out what you're typing.

Going deeper into this "sensor based side-channel" rabbit-hole lead us to [this paper by some top Stanford folks](https://www.usenix.org/system/files/conference/usenixsecurity14/sec14-paper-michalevsky.pdf) which showed how gyroscope on a mobile phone is sensitive enough to capture audio surrounding the device. Since these guys had used only gyroscope, we decided to see if accelerometers (or a combo of them both) could be used to do this too.

_I'd be remiss if I didn't mention here that all of these attacks have only been performed in controlled environments and their practical application seems questionable to me._

My work started off well - I created an android app to record sensor readings but we then digressed into a different sensor platform which didn't really work out. I only had time to do some basic analysis work, but the results turned out to be positive. You can read the details in the [project report](https://github.com/dufferzafar/accelphone/blob/master/report/Thesis.pdf) or have a look at the [code I wrote](https://github.com/dufferzafar/accelphone).

I didn't want to continue this project because it involves way more signal processing than my brain can handle and It also turned out that Android P will prevent apps from recording sensor data silently in the background making these attacks even more impractical (in their current form.)

## TA Work

I TA'd the "Intro to CS" (COL - 100P) course taught by Prof. Kolin Paul and like last semester - got the job of creating the Moodle/VPL programming assignments. The work was very light since I already had a good handle on how VPL works and all the harder assignments were created by one of my seniors.

## Notes

Even though I make notes during class (or atleast I try to), I almost never read them and instead prefer someone else's version. [^2]

So I used Khushboo's [notes for HSN](https://drive.google.com/open?id=1Pw2uqFXvx7J_oCkoWm15ePAPyR1LplOm) and [Harish](http://github.com/hthuwal)'s [notes for ML](https://drive.google.com/open?id=1z3Qd-BzdDx7Q6_doYUTZ3Xi3vuAiQjfd). 

There's also [these ML notes](https://drive.google.com/open?id=1-bIWAUMdv9jQnGSmT7AyLsCrpgUTCZIF) by [Suyash](https://github.com/ozym4nd145), which I didn't go through, but they look neat.

## Result & Future

Grades turned out to be much better than I'd anticipated, I scored 10 in NSS, 9 in HSN, 7 in ML and 10 in Minor resulting in an SGPA of 8.92

For the next semester, I need to take one course along with a major project. I haven't quite decided what the course will be; some options are: "Cloud Computing", "Data Mining" and "Wireless Networks".

My major will _probably_ be on understanding and modifying the [core Bitcoin code](http://github.com/bitcoin/bitcoin/) to implement some new ideas (which've already been thought by Sir and one of his student.) I like the project because it is essentially a GSoC (which I'm supposed to be good at.) The deliverable is clear and the challenge is obvious - learn enough C++ to deep dive into a 400,000 LOC codebase. I've always felt that not developing C++ software is one of the biggest mistakes I've made, so if nothing else comes out of this project, I hope I'll learn enough C++ to be able to work on projects that I've always wanted to: [Clementine](https://github.com/clementine-player/Clementine/), [Dolphin](https://cgit.kde.org/dolphin.git/) (among other KDE applications), [OpenAge](https://github.com/SFTtech/openage/), [Endless Sky](https://github.com/endless-sky/endless-sky) etc.

<br /> <br />

---

<br /> <br />

[^1]: I'm _quite_ proud of [the Makefile](https://github.com/dufferzafar/solid-media/blob/master/Makefile) that I wrote for this project.

[^2]: I whole-heartedly blame [Mittal](http://nickedes.github.io/) for this, who spoilt our entire B.Tech batch by his amazing notes.
