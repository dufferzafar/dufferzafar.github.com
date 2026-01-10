---
redirect_from: /2014/06/25/the-current-state-of-things/
layout: post
title: "The current state of things."
date: 2014-06-25 15:14
---

I didn't write the weekly review post I was supposed to the last week and won't be doing it this week either (or the weeks to come) as I now see no point in writing them - why'd anyone be interested in reading my journal entries?

Instead, I'll be writing a *meaningful* post every week, most probably on Tuesdays, but I can't promise that as I have a quite tight scheduly right now.

This month has been the busiest one of my life, I've never worked this much before. As you might have guessed from my weekly posts <!-- more -->, I have an awful sleep cycle. I sleep at [4 in the](http://www.ted.com/talks/rives_on_4_a_m) [morning](http://www.ted.com/talks/rives_a_museum_of_4_o_clock_in_the_morning), wake up at 11-ish the next day, and then work like crazy. 

I like to believe that the thing that's keeping me so occupied is GSoC (but I can assure you there are other variables at play.)

The GSoC project is coming along nicely (and slowly.) The website is [now live](http://picard.mbsandbox.org/) at one of MusicBrainz's servers. It's not finished though, as I still need to import the Picard documentation from the MusicBrainz (MB) Wiki but am pretty bored of all the web tech, so I'll do it after I create the Picard interface for downloading plugins which can only happen after I fix the script that generates JSON data from plugins. In short, there's still a lot to do.

When I chose this project from the MB idea list, I knew that the work was too easy, I thought I could do it in like two weeks, but I seem to to be moving at a snail's pace and it's all because of the *other* stuff that catches my fancy.

Not being able to stick with projects has been one of my biggest shortcoming. I switch projects more often than I change clothes, so I'm usually working with 3-4 things at once. The downside is that none of them really get done, but the benefit is that I get to learn different technolgies (something I feel is the sole reason of my existence.)

Some time ago I was really excited about, and working on, a project called [IdeaBin](https://github.com/jdevlabs/Ideabin/) which is supposed to be a website that'll host people's ideas (mostly mine, as I don't feel there'll be anyone else using it.) The last [commit](https://github.com/jdevlabs/Ideabin/commit/fde313b780ab9fab1199ea4842b30a97ad76e2f8) I made on IdeaBin finished the API endpoint that can list users. The next obvious step is to add the ability to create users. I was going to do that but then stopped myself because I want [Shivam](http://trigonaminima.github.io/) to catch up as this was his idea originally and he really wanted do this, so I won't be making any further updates until Shivam adds something, but sadly he is pretty busy himself with his internship. Maybe we'll work on this once the college reopens.

The other thing that I've worked on this summer are [Userscripts](https://github.com/dufferzafar/userscripts) that import data to [MusicBrainz](https://musicbrainz.org/). I started by creating an importer from Amazon. The script has little practical utility (mostly because Amazon has shitty data and an even shittier format) and is generally useless but it helped me learn a few core things so I could hack on other scripts easily.

The next script I wrote is for [T-Series](http://www.tseries.com/). After creating the Amazon one, this was fairly simple to code but it really didn't serve a purpose because even though T-Series has some data it is mostly incomplete (e.g: the track lenghts are missing.)

The only script that's worth using in the real world is the [Import from iTunes](https://github.com/dufferzafar/Userscripts/blob/master/MB-Import-From-iTunes.user.js) one. It was originally created by [someone](http://userscripts.org:8080/users/41307) else and I've modified it to suit my needs. Now, whenever I need to add a release (which is after I listen to a song that I like and is not on MB) - I just use [fnd.io](https://fnd.io/) to find the release on iTunes and then use the script to import the data. There are a few things that I'd still like to add to the script, like the ability to search the MB database and display if the release is already on MB, so I don't have to search for it in a separate tab.

Next in the list is [Ping](https://github.com/dufferzafar/Ping) (blame [Aditya](http://kwikadi.wordpress.com/) for the terrible name) - the thing I was excited about until yesterday. Ping will be an application developed using [Node-Webkit](https://github.com/rogerwang/node-webkit/) that'll display notifications from multiple social services in one place, so you don't have to visit the sites just to see if there's something that you should know. We'll start with Facebook and Github integration as those are the two sites I use the most. The app will have an extensible structure so anyone can can add a new service with ease. I helped [Anzal](https://www.facebook.com/anzal.khan.12) and [Nikhil](https://www.facebook.com/nikhil.mittal.5682) setup the environment for developing Ping on their machines but Anzal is still having some problems. <!-- Being able to build something from sources on your machine is half the battle. -->

I would've worked on Ping now, had I not struck upon yet another idea yesterday - a GSoC search and statistics website. I don't quite like the interface melange provides to search [Organizations](http://www.google-melange.com/gsoc/org/list/public/google/gsoc2014) and [Proposals](https://www.google-melange.com/gsoc/projects/list/google/gsoc2014), so I'm planning to create an alternate interface (in [AngularJS](https://angularjs.org/) and [Bootstrap](http://getbootstrap.com/)) that'll be visually pleasing and fast. The plan is to scrape all data from the melange site (using [Scrapy](http://scrapy.org/)), store that data as JSON (which will help other people too), and then create a search interface using Angular. 

To add to the project, we could also display some kick-ass statistics from all the data (Shivam would love this.) I'll use [d3.js](http://d3js.org/) for all the stats as I have some [experience](https://github.com/dufferzafar/personal-analytics) with it (though I might have forgotten, as I used it some time ago.)

The project will serve other purposes like a.) Aditya will get to know real world JS, b.) I'll gain some experience with Angular (we'll need it when we create a web client for IdeaBin), c.) We'll find out some nice orgs and projects during the process which will help us for the next GSoC (I know I really shouldn't be thinking about the next gsoc when I'm still running behind schedule on this one, but, what the hell!)

So I'll probably be working on this gsoc s&s thing, along with picard now.

There are still a few more ideas floating in my head that I'm yet to decide something about. Like adding FB chat integration (via XMPP) to [Komanda](https://github.com/mephux/komanda) (which is a pretty slick IRC client, created using node-webkit.) Or I could team up with Aditya and add some features to [InstantBird](http://instantbird.com/) (which is yet another messenger, built with mozilla's tech.) Adi and I planned to write a blog post about the state of desktop IMs where we'll discuss things in detail (if we ever write that post.)

Yet another thing I could work on is [jdlbot](https://github.com/jdevlabs/jdlbot) - a [hubot](https://github.com/github/hubot/) that we'll be using with [Slack](). I've tested it on Windows and just need to deploy it on a server, I tried doing that on [Heroku](http://heroku.com/) but that didn't work as I have an unverified account and for some reason Heroku was declining my credit card credentials. The hackiness of hubot excites me tremendously, but setting up stuff on servers is not much fun :/

I also had an idea of creating an [Autohotkey](http://ahkscript.org/) script that grabs and uploads a screenshot to Slack. I googled it, but couldn't find an easy way to POST multipart/form-data in AHK. The obvious workaround would be to grab screenshot in AHK and use [cURL](http://curl.haxx.se/) in the background to upload it, but that makes the script too trivial :/

There's [CrAnK](https://github.com/jdevlabs/CrAnK) too, which was supposed to be a tool that can automatically crack simple ciphers. My love for cryptography (and number theory) ranks second only to my love for building things, and this was the project with which I could achieve both :/

The last item on the list is this blog itself. I want to write more posts ([filled with](https://github.com/dufferzafar/Cmder) [all sorts of](https://github.com/pranavraja/tldr) [awesome](https://github.com/maebert/jrnl) [stuff](https://github.com/azac/sublime-howdoi-direct-paste)) and complete some [half-written](http://dufferzafar.github.io/blog/2013/12/24/tools-for-windows-developers-and-power-users/) drafts but I just can't find the time. I need to work on the design too (like this [categories](http://dufferzafar.github.io/blog/categories/) page looks awful.) I also have plans to write an About page and a few other pages and Oh! I still don't have a super sexy home page :/

This post got way longer than what I'd thought, so if you've read it all, thanks a lot. I owe you one.
