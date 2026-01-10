---
redirect_from: /2015/06/14/how-i-listed-ids-of-all-my-facebook-friends/
layout: post
title: "How I listed IDs of all my facebook friends"
date: 2015-06-14 00:40:40 +0530
---

I've been working on grabbing data from Web 2.0 sites like Facebook, Github, Last.fm etc. The plan is to come up with something kick ass to do with all this data. But first, we need to grab it all!

I put together a script to download all my Facebook wall posts, and was now working on something that could download all my personal conversations. Luckily, [this script already exists](https://github.com/RaghavSood/FBMessageScraper) and all it needs is a Conversation ID.

Now all I need is a list of facebook IDs of all my friends and we'll be done, but there doesn't seem to be a direct way of getting all of those or maybe there is, but who has the time to read [boring api](https://developers.facebook.com/docs/graph-api/reference/v2.3/conversation) [docs](https://developers.facebook.com/docs/graph-api/reference/v2.3/conversation/messages)?

<!-- more -->

Here's what I did:

I loaded the [Messages page](www.facebook.com/messages/) on my Firefox and scrolled the conversations list on the left to the bottom. This step was easy as I don't have many friends.

I right-clicked one of the conversations and selected 'Inspect Element'.

I found a `<ul>` element with id `wmMasterViewThreadlist` that contains a list of `<li>` tags, each of which represents a conversation - neat!

I right-clicked the ul tag, selected 'Copy Inner HTML' and pasted it into Sublime, this gives us a raw HTML containing a lot of stuff.

In Sublime, I searched for the regex `recent:user:\d+` to get all users I've talked to. After some slicing 'n' dicing, I had a list of IDs of all my friends.

But this does not include the group chats. To get them, you need to look for `conversation-\d+`.

Once you have a list of IDs in a file, say 'friend-ids.txt', you can do things like building a dictionary of all your friends using nothing but a shell pipeline (which took me about 30 minutes of trial and error to write, shoutouts to Rizvi Coaching Classes.)

``` bash
cat friend-ids.txt | xargs -I {} sh -c "curl -s graph.facebook.com/{} | jq -c 'select(.name != null) | {name: .name, id: .id}'" | tee friend-list.txt
```

## Further thoughts

For people who are lazy or have a long list of friends, I think this method can be automated using a headless browser. Maybe [Python Mechanize](https://pypi.python.org/pypi/mechanize/) or [Selenium](https://selenium-python.readthedocs.org/)?

Open Facebook. Log In. Go to messages page. Get all children of 'ul#wmMasterViewThreadlist' and extract needed data. Sounds easy!
