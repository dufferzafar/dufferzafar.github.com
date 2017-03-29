---
layout: post
title: "Sharing Code - Github repositories"
date: 2013-09-29 18:08
---

Writing code is one thing, but sharing with the world is a different story altogether.

I have chunks of code scattered all over my hard drive. Some of it is pretty naive while the others are really cool. Some solve a particular problem while some are just proof-of-concepts. They are all worth sharing nonetheless.

<!-- more -->

I have a few repositories on github where most of my code is hosted. The only thing that stops me from pushing all my code to github is the fear that It’ll end up half-assed. And I don’t want to do that.

The scripts that I write mostly contain dirty hacking – code that just works. They are written with just one thing in mind after all and that is to get the shit done. Now, I don’t want anybody to read my dirty code, that’d be crap right?

So before pushing anything onto github I try to ensure that my code meets some standards. It should be readable even by a newbie, extensible so that people can add their own fragments. I add comments to make sure the reader gets what’s exactly happening.

This process, the one wherein I ensure code quality is time consuming and a bit boring if you ask me, but it’s necessary and just can’t be ignored.

Most of my Github repositories are in a pretty abject state. It’s been in the last month that I’ve started paying them the attention that they deserve.

I created [Win-Butler](https://github.com/dufferzafar/win-butler) last week by merging some of my existing scripts. Most of the code was already written and all I had to do was assemble the chunks, remove crap and add comments. It took me about three hours to do so but I am fairly happy with the output. The script is clean and can be easily edited. Also, it felt great to churn out some AHK after a long time.

I’ve polished [Autohotkey-Scripts](https://github.com/dufferzafar/Autohotkey-Scripts/) – redundant scripts have been removed, new ones added. I’ve also added readmes to some the of scripts. There’s still a lot of work to be done – I need to further cleanup most of the code, add remaining readmes. I also have some viruses/pranks scripts written that I need to refine and push.

[AMS-Projects](https://github.com/dufferzafar/Autohotkey-Scripts) has been updated with the readme. I don’t plan to further improve anything.

[libLua](https://github.com/dufferzafar/libLua) is a real mess. There’s no documentation on what functions are available, the code files themselves are scattered and need to be standardized. I think I should separate bigNum into a separate repository as it really is worthy of some attention.

[Project-Euler-Solutions](https://github.com/dufferzafar/pranks-and-all) – The only reason I uploaded these solutions was because they were solved in pure Lua. I coded from scratch any dependency that I needed (bigNum is an example.) This repo is a mess too. I can scrub most of the solutions and could probably increase the efficiency of some.

[Shar](https://github.com/dufferzafar/ShaR) - This algorithm is so naive that I wouldn’t even have uploaded the code had it been in any other language. But you can’t just throw away code written in Lua. As of now the cipher is amateurish and there isn’t much hope for it but still I think I’ll rewrite the code someday, write a readme too. Till then…
