---
redirect_from: /2015/08/16/yet-another-github-streak-hack/
layout: post
title: "Yet Another Github Streak Hack"
date: 2015-08-16 21:29:59 +0530
---

I wrote about a Github streak hack some time ago which involved changing system date to make commits in the past. How lame.

While the previous hack would could be used to fill gaps in your streak, the one I found today will allow you to massively increase the number of commits you've pushed.

<!-- more -->

<!-- I might be the first one to write about this since I couldn't find it anywhere else. -->

<!-- Like most things, I found this by chance when I pushed some commits after a rebase and Github started showing me weird commit counts. -->

This trick involves knowing some non-beginner stuff about Git, like what a reachable commit is, what a `git rebase` is and what it does to your repository. 



It'd also help to learn what `@~3`, `HEAD` mean. 

Github calculates your contribution activity by the number of unique commits that you push. In a repository with history that's not modified, things are alright; but once you start tampering with your history, doing a rebase for example, things get pretty interesting.

So let's say you have a repository with 10 commits. Your contribution activity will show something like "Pushed 10 commits to ..."

Now if you modify an older commit - for eg. using an interactive rebase to change the commit message of @~7 - all the commits from @~7 to HEAD will get new identities (SHA-hashes) as a commit below them was modified. 

Once you force push these commits to Github, they'll be counted again in your contributions chart. So your activity will change to something like "Pushed 17 commits to ..." whereas if you look at the commit list of your repo it'll still show 10 commits, since the others are not reachable from `HEAD`.

<!-- 

http://stackoverflow.com/questions/2304087/what-is-head-in-git

http://www.gitguys.com/topics/head-where-are-we-where-were-we/

http://nathanleclaire.com/blog/2014/09/14/dont-be-scared-of-git-rebase/ 

http://stackoverflow.com/questions/804115/when-do-you-use-git-rebase-instead-of-git-merge

http://rypress.com/tutorials/git/rebasing

http://eagain.net/articles/git-for-computer-scientists/

http://stackoverflow.com/questions/4111844/what-does-reachable-unreachable-mean-in-git

-->



If you want to know what it looks like 
