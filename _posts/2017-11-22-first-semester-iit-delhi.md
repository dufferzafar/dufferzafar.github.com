---
layout: post
title:  First Semester at IIT Delhi
date:   2017-12-01 23:17:47
---

My first semester of M. Tech at IIT D has ended.

I had three courses this semester (all of which were compulsory): 

* Introduction to Logic and Functional Programming (ILFP) by Sanjiva Prasad
* Advanced Data Structures and Algorithms (ADA) by Sandeep Sen
* Software Programming Lab

<!-- more -->

### Introduction to Logic and Functional Programming

This was a very unique course - one that I would never have taken by choice, but having passed, I'm sort of glad that I did. There was a bunch of really cool things I learnt, perhaps the most important of which is the OCaml language. We did 6 assignments in OCaml that involved modeling some logical structure like Sets, Proof Trees etc. One of the defining features of the language is its strongly typed nature. I'd always read how static typing could prevent bugs etc. but getting to see it myself was a good experience. Projects like mypy do make some sense to me now - just knowing the type of every object makes reasoning about the code easier - both while developing and debugging. 

As always, all the code I've written can be found here: [https://github.com/dufferzafar/oh-camel](https://github.com/dufferzafar/oh-camel)

This was a pretty challenging course and for several reasons:
    
* There was no book to follow

It's not like there are no Logic textbooks, but the problem is that everyone uses different syntax and presents topics in different orders which is enough to scare off a novice.

* We had no roadmap

The topics were presented in an arbitrary order and there too we'd have no idea of why we were doing something (e.g: why does proving this result matter.) Sometimes things would make sense weeks down the line, but not always. There's a ton of stuff I have in my notebook that just makes zero sense to me.

### Advanced Data Structures and Algorithms

This was a standard Algorithms course. We started off with familiar stuff like Shortest Path Algorithms etc. but later learnt a few new things like Skip Lists & KD Trees. The major difference from my undergrad course was the focus on proving correctness of algorithms.

There were two easy programming assignments as well - Rank Selection & Edit Distance. I wish there'd been more programming involved. Coding up a non trivial data structure would've been cool!

The code is here: [https://github.com/dufferzafar/adv-ds](https://github.com/dufferzafar/adv-ds)

### Software Programming Lab

This was the highlight of the semester and took up most of my time. It was a different kind of course too - no classes, no labs, just assignments - three in total, each from a different domain. I partnered with Harish (who is also from Jamia) on all three of the projects.

The assignments were (links to GitHub repositories):

* [A Bitcoin-like Distributed Ledger](https://github.com/dufferzafar/distributed-ledger)
* [A Ludo playing AI bot](https://github.com/dufferzafar/ludo-bot/)
* [Data Analytics using Hadoop](https://github.com/dufferzafar/github-analytics/)

The ledger was a tricky project because we didn't have much knowledge of distributed systems so we couldn't understand most of the assignment until much later. It was also the one where we learnt a lot - distributed hash tables (esp. [Kadmelia](https://en.wikipedia.org/wiki/Kademlia)), basics of Blockchains, [Mininet](mininet.org/) & above all - Python AsyncIO. We started with an [existing implementation](https://github.com/chrisguidry/kademlia_aio) of the Kademlia protocol using asyncio and then modified it later to suit our needs. We couldn't finish all the sub-tasks (like Lamport Clock IDs etc.) but our presentation went pretty well.

The Ludo bot was conceptually straight forward but, being the procrastinators that we are, we started really late and only had the time to implement some simple heuristic based [strategies](https://www.researchgate.net/profile/Faisal_Alvi/publication/224259871_Complexity_analysis_and_playing_strategies_for_Ludo_and_its_variant_race_games/links/558f6d7a08ae47a3490d9d72/Complexity-analysis-and-playing-strategies-for-Ludo-and-its-variant-race-games.pdf) which turned out to be weak against other bots. The game board was drawn using PyQt's GraphicsView API and involved lots of manual positioning and hair-pulling. 

Data Analytics was another project where we learnt a lot mostly because we'd never done something like it before. We decided to use the GitHub dataset mostly because we knew what the dataset would contain (or atleast we thought we did.) We were given a cluster of 4 virtual machines on IIT D's local cloud, a total of 320 GB HDD and 20 GB RAM. Setting up Hadoop & Spark on the cluster took most of our time but once the setup was done, the rest was easy, we just used a JupyterLab notebook to run Spark queries. I have a lot more to say on this, so I might do a separate blog post. Stay tuned!

## TA Work

I was a TA for an Introduction to CS course, where my work was to create programming assignments and quizzes to IITD's [Moodle](https://moodle.org/) using the Moodle-VPL plugin.

Moodle is one of those pieces of software which are held together in place using a lot of safety pins. Things just barely work. There's little to no extension possible. The documentation is scarce. Most importantly, the code is hard to understand - all the $ symbols make my head hurt.

Harish also worked with me on this. The code we wrote to create assignments is available here: [https://github.com/dufferzafar/col-100](https://github.com/dufferzafar/col-100)

The TA work is paid so I've been getting ₹12,000 on every 1st of the month, including today :)

## Notes

Harish makes really good notes and with the help of CamScanner I converted them to PDFs. [Here they are](https://drive.google.com/drive/folders/1BsWuAbrOppKATdcxeuCjkiplDPTmSy_1?usp=sharing). 

## Result & Future

I scored A in COP - that's 10 points. B- in ILFP (8 points) and B in ADS (7 points) for a total SGPA of 8.1 which is good enough for me.

I have high hopes from the next semester though mostly because the subjects will be of my interest. I've chosen "Advanced Computer Networks" and "Network & System Security". There's also a DBMS course which I'll try to get waived (by clearing a test.)

Next semester also has a "Minor Project" for which I'll most probably be working on something Security related under Prof. [Vinay Ribeiro](http://www.cse.iitd.ernet.in/~vinay/).
