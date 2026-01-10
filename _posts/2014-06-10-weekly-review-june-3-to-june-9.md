---
redirect_from: /2014/06/10/weekly-review-june-3-to-june-9/
layout: post
title: "Weekly review - June 3 to June 9"
date: 2014-06-10 22:12
---

*I think I've got into the habit of writing these. Good for me.*

I got quite a lot of work done this time, mostly because I had my facebook chat turned off for most part of the week. Here is a date-wise breakup:

<!-- more -->

On tuesday I got my laptop's memory upgraded to 8 GB (but didn't get the performance bump I was expecting.) Keeping up with my no-gsoc-on-tuesday policy, I just spent the day writing the blog post and chatting. During the night though, something new happened. I was idling around on #ahk when I found this guy (Rickard) from Sweden who had some problems with a script he was trying to write. I helped him and found out that it was some sort of a DDoS tool he was trying to write (only for educational purposes, or so he said.) I had a long conversation with him and we started cooking up some top secret stuff in one of those private Github repos of mine.

Manic Time tells me that I spent 3 hours 49 mins and 58 seconds chatting on Wednesday. Maybe it was this figure that made me turn off pidgin. I did a little bit of work on my [Userscripts](http://github.com/dufferzafar/Userscripts) during the day and wrote some top secret code with Rick at night.

Thursday was nice, as I spent just about 20 mins on Pidgin (probably my all time low) which means I had more time to focus on writing code and thats exactly what I did. I created a [downloads page](http://musicbrainz.github.io/picard-website/downloads.html) for Picard's website. In case you want to know where I copied this one from - it was [Apache friends](https://www.apachefriends.org/download.html).

I spent most of the Friday playing a really old hacking game called [Uplink](http://www.introversion.co.uk/uplink/hackerelite.html) with my brother. This was not the first time I was playing it, but I still had problem doing some of the missions. The game is a must for anyone who has the slightest interest in hacking. During the night, I spent creating a project structure for [IdeaBin](https://github.com/jdevlabs/Ideabin/). I read a lot of literature on how to setup flask apps properly and finally settled upon the [one](https://github.com/mitsuhiko/flask/wiki/Large-app-how-to) from the creator of flask himself.

On saturday, I did some more work on IdeaBin (like unit tests.) I then created a templates system for the Picard website so that we don't have to include common code like footer, navbar etc. on all html pages. For this task I simply used a gulp plugin that can [include files](https://www.npmjs.org/package/gulp-file-include) and added a task to my gulpfile. I also watched "The secret life of Walter Mitty" which turned out be a meh! movie, it had a nice soundtrack though.

I didn't work much on sunday as I had to run errands for my mother but I still managed to create a basic view for the IdeaBin API which saved my day from being labelled as wasted.

I added a page to the Picard website which fetches the changelog from Picard's Github repo and displays a [nice html version](http://musicbrainz.github.io/picard-website/changelog.html) of it. I finished up the day by writing the mail to MB-Devel. At night, I watched "Shudh Desi Romance" which is a nice movie to watch at night. It made me quite giddy so I just cuddled up my pillow and slept...
