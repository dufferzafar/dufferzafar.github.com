---
title: "Qarz-e-Hunar"
date: 2026-05-01
---

Aaron Swartz, on a stage in the sun, microphone in hand: *programming is a superpower. It's meant to change the world.*

![Me and Guddu at our desk in Gurgaon, August 2010](/images/Shadab-Mehtab-20100812.jpg)

The pendrive cost ten rupees an hour. Sometimes twenty, if I felt rich.

We didn't have internet at home. So my routine, after school, was to walk to the cybercafe near our house, pay the man at the counter, and start scraping. Tutorials. Conference videos. PDFs. I never *consumed* anything in the cafe — I was an optimizer you see. I'd fill the pendrive in 30-60 minutes and consume at home, at the desk you see in the photo above. My younger brother [Mehtab](https://blog.mzfr.me/) — Guddu — would visit during holidays and we'd sit there hunched together, learning what we could.

That was the afternoon. I was eighteen. I had been thinking about computers all my life. And here was a young man on the other side of the world telling me the thing I did with my hands was a *superpower*.

For an 18-year-old kid in the capital of India, that was — I still don't have the right word. *Permission*, maybe. Permission to take this thing seriously.

<!-- more -->

## tl;dr

- I owe my career to open source. Specifically, to MetaBrainz and three GSoC summers between 2014 and 2016.
- I was also exactly the kind of "drive-by" Indian contributor that maintainers like [ruaok](https://blog.metabrainz.org/author/ruaok/) and [Maximilian Hils](https://news.ycombinator.com/item?id=14020814) complained about. I left when the stipends did.
- Ten years later: two DuckDB patches, a salary that covers the time, and a young neighbor named [Adeeb](https://github.com/Dewolf1/) whom I'm trying to push toward GSoC.
- This is the debt of craft. I owe it. I'm starting to pay it back.

## the discovery

Sometime in 2013 or 2014, [Richard Stallman](https://en.wikipedia.org/wiki/Richard_Stallman) came to Delhi.

Some of us — [Shivam](https://shivamrana.me/), me, [Tushar](https://www.linkedin.com/in/tushar-raheja-bbab51118/), maybe [Nikhil](https://www.linkedin.com/in/nickedes/) — went to the talk. I think it was at Acharya Narendra Dev College in Govindpuri. We were undergrads at Jamia, fresh and starry-eyed. RMS shuffled onto the stage with an old laptop that looked silly even by 2014 standards. He was a fat man, and at one point when he took his jumper off, his belly showed and the kids at the back of the hall started giggling. They had no clue who the guy was.

I didn't laugh. I sat there enamored, listening to him talk about the GPL, gcc, the four freedoms. On the bus back to JMI I wouldn't shut up about him. I think I gave Tushar an entire history of GNU.

He gave out free FSF stickers that day. I think I still have one somewhere.

---

A few months later, Shivam came up to me with a glint in his eye.

> "Bhai ek org hai jo music ka andha data collect karti hai. GSoC karte hain."
>
> *(Bro, there's an org that collects insane amounts of music data. They do GSoC.)*

The org was [MetaBrainz](https://metabrainz.org/). I went home that night, found the GSoC ideas page, and got obsessed. We already knew about GSoC because [Akif bhai](https://www.linkedin.com/in/akifkhan1/) — a senior at Jamia — had done it the previous year. He was the local proof that this was possible for kids like us.

I applied to MetaBrainz. I got in.

My 2014 project was [MusicBrainz Picard](https://picard.musicbrainz.org/) — the cross-platform music tagger. I built the website you see at that URL today, and added in-app plugin downloads to Picard itself. It was my first foray into Python/Qt desktop apps. Robert Kaye — *ruaok*, MetaBrainz's founder — was running things from somewhere in Europe, and the whole community lived on `#metabrainz` and `#musicbrainz` on Freenode. My handle was `dufferzafar`. Still is.

I remember Shivam reading my first IRC messages and laughing the next day:

> "Tu kitna humble hai re. *(How humble you sound, dude.)*"

I was confused. Wasn't that how you talked online?

It took me years to realize I was IRC-polite in the way only a kid who grew up writing "Respected Sir" at the top of every school exam could be. Westerners read it as deferential, weird, very-online-Indian. The [Maximilian Hils](https://news.ycombinator.com/item?id=14020814) of the world were used to terse, blunt, "ship it" Slack-speak. It was the tiniest cultural friction. But it was *there*.

## dhandhera

Summer of 2014. The work happened from my nani's house in Dhandhera, a small village near Roorkee.

No AC — just desert coolers humming loud enough to drown the azaan. Powercuts, of course. I had an MTS dongle for the internet[^mts] and a Dell laptop I'd bought during my first year of BTech. Family understood I was "working for Google" — close enough.

[^mts]: I lived on a 7 GB/month prepaid plan. Monitoring bandwidth was so critical that I [wrote a Linux usage tracker](https://github.com/dufferzafar/netuse) for it because Networx didn't exist for Linux. 160 stars later, that repo is a strange little artifact of how thin a thread Indian internet hung from in 2012.

My schedule was inverted: bath at 10:30 PM, dinner, then sit at the desk till 6 AM. The IRC channels were busiest at 2-4 AM IST — that's when the Europeans and Americans were online, which is when my mentors were online, which is when the work happened. I'd sleep through the day, wake up around 4 PM, do some goofing around, and start again.

People in the village would walk past our open gate at strange hours and see me hunched at a screen. Some of them asked Guddu:

> "Tera bhai kya karta rehta hai raat bhar?"
>
> *(What does your brother do all night?)*

He didn't always have an answer.

---

At the end of that summer Google paid me ₹3 lakhs[^stipend].

[^stipend]: GSoC 2014 stipend was about $5,500. ₹3 lakh in 2014 was real money for a 20-year-old in India. Across three GSoCs (2014, 2015, the part-stipend in 2016), it was close to ₹10 lakh. You'll see why that exact number is load-bearing in a moment.

When I was in class 2 or 3, my mom had taken a loan of ₹3 lakhs to buy a small house in Vijay Park, Maujpur, Delhi. After my parents separated, that loan stood against her teacher's salary at Zakir Hussain school in Jafrabad. It took her years to pay off. She has been afraid of loans ever since, and has imparted that fear to all of us[^loan].

[^loan]: There is no shape of post in which I can talk about my mom for the right amount of time. So I'm going to leave most of it for elsewhere. The relevant fact for this post is: she paid back a 3-lakh loan over a decade of teaching school. I made the same number in three months. The exchange rate of effort to money was the most violent thing I had ever felt.

When I received that first GSoC stipend, the only number my brain could compare it to was that loan. *One summer of typing on IRC at 3 AM, and I had matched a decade of my mother's salary.*

## the fall

I came back the next year — 2015 — for [CritiqueBrainz](https://critiquebrainz.org/). It was a Flask app for music reviews. My mentor was [Roman Tsukanov](https://github.com/gentlecat). I picked the project because Flask was familiar; I wanted something I could ship without learning a new framework. There aren't many memorable beats from that summer. It was easy. I was getting good at this.

Then came 2016.

I applied for a third GSoC with MetaBrainz. By this point I'd been on `#metabrainz` for two summers, but my contributions had been almost entirely seasonal — turn up in March, ship through August, vanish till next March. Ruaok had noticed.

He sent a message that, paraphrased from memory, went something like:

> *Shadab, we're not going to take you this year. You only show up for the GSoC period and then disappear, which is against the spirit of the program. If you stick around as a non-GSoC contributor for the year, we'll consider you next time.*

[Aditya](https://github.com/kwikadi) — another close friend — was on the channel and immediately started DMing me damage-control advice. *Don't tell him this is your final year. Don't say you won't be a student in 2017. Just nod and say you'll stick around.*

Reader, I told him exactly that. *"Robert, this is my BTech final year. I won't be a student next year."*

I felt shamed. I tried to weave my way out of it. I couldn't. Ruaok had drawn the line cleanly and I had walked over it onto the wrong side, on public IRC, in front of everyone.

I pivoted. I applied a second time that year — to [Mitmproxy](https://mitmproxy.org/) under [Honeynet](https://www.honeynet.org/) — and got in. The work was real: I led the Python 2 to Python 3 port of major internal libraries, and made scattered improvements through the summer. My mentor was Maximilian Hils.

Even though I kept up with the project, I never contributed to Mitmproxy after that summer ended.

---

April 3rd, 2017. I was sitting somewhere in Delhi waiting for my GATE results when I read a [comment on Hacker News](https://news.ycombinator.com/item?id=14020814):

> *I'm a GSoC org admin for a few years now. To be honest, the bureaucracy that comes with GSoC is really negligible from my point of view. The application form is fairly short, the evaluations during the summer are literally done in five minutes... there really isn't that much overhead.*
>
> *The part that takes a lot of time for us is mentoring students. You'll very likely invest more time into the student than it would take you to write everything yourself (which also would be more fun). **Unfortunately, some students don't stick around**, but if everything works out, you'll get fantastic long-term contributors (we did). The upfront investment on the mentor's side may not be everyone's cup of tea (and that's ok), but I think it's unfair to attribute that to bureaucracy. GSoC may just not be a good fit for OpenBSD in that regard.*

The author was Maximilian Hils — who had just spent a summer mentoring me.

I knew, the second I read it, that I was the student who didn't stick around.

क़र्ज़ की पीते थे मय, लेकिन समझते थे कि हाँ<br>
रंग लाएगी हमारी फ़ाक़ा-मस्ती एक दिन

*(We drank our wine on credit, but we always understood —<br>
that this hungry merrymaking of ours would, one day, bear color.)*[^ghalib]

[^ghalib]: Ghalib. The whole sher is a small confession of debt: we knew we were drinking on someone else's tab, but we trusted the future to vindicate us. GSoC was that exact bargain. Three summers of stipends taken with the half-conscious assumption that the destitute revelry would eventually pay for itself in craft.

## the indianness of it all

Here's the thesis. I want to be plain about it.

Open source contribution, as it's practiced in the West, quietly assumes a social safety net and a career ladder that doesn't punish you for spending a summer unpaid on a volunteer project. Indian students don't have that. Cut-throat competition starts in school and escalates through college; the pop curve is what it is, unemployment is what it is, and we all need to outwork each other to stay afloat.

Our generation showed up for the stipend, learned real craft, and then vanished into jobs that demanded everything we had — exactly the pattern Ruaok and Max named on IRC and HN. They weren't wrong. I was one of those students.

And I wasn't alone.

- Shivam, who introduced me to MetaBrainz, never did GSoC. He went on to do excellent work elsewhere, but the OSS hobby never stuck.
- Akif, our inspiration, did one GSoC at OpenSUSE in 2013 and (as far as I can tell from the outside) drifted into industry like the rest of us. I have nothing but respect for him; without him I wouldn't have known the program existed. But the pattern holds.

It wasn't that any of us *didn't want to*. I wanted to keep contributing. I genuinely did. But you finish your degree, you take the job that pays the rent or the loan or both, and then college courses and projects and exams give way to OKRs and standups and on-calls. The incentive evaporates. The maintainers in Berlin and Amsterdam and Barcelona keep going, because their lives have room for it. Ours don't.

This is not an excuse. It is, I think, an explanation.

## the crater

Between 2016 and 2026 there is a ten-year hole in my open-source life.

I joined Adobe straight out of Jamia in mid-2016 — a sweet placement, a fat package, a famous company. The role turned out to be writing Selenium-based unit tests in Python. After two weeks of staring at it, I'd convinced myself a 12th-pass kid could do this work. Over lunch, my friend [Prerit](https://www.linkedin.com/in/prerit2010/) and I quietly decided to resign together and prep for GATE. My manager was *furious*:

> "I'll make sure you're blacklisted from Adobe."
>
> "Adobe has invested so much in you already. Is this how you repay?"

The word *repay* sticks with me to this day, given everything else this post is about.

I gave GATE in February 2017 — AIR 59 — and joined IIT Delhi MTech CS in June. The course load was brutal. I realized fast that hobbyist programming would have to die if I wanted to actually do well in MTech, and as much as it pained me, I let it die. From 2017 to 2019: little to no hobby OSS. In June 2019 I got placed at [Tower Research Capital](https://www.tower-research.com/), where I have been ever since[^trc].

[^trc]: TRC is a quantitative trading firm doing serious systems work — low-latency C++, custom file formats, in-house storage engines. The day job is intellectually rich and it pays absurdly well. I've written elsewhere about the [moral dissonance](/2025/12/30/saarthi/) of working in HFT and the [career path that didn't happen](/2026/01/14/civil-service/). What that day job *didn't* leave room for, for a very long time, was open source.

So: ten years. Few public PRs. No IRC. No mentoring. Freenode/Discord kept buzzing without me, exactly as the mentors had predicted.

## the return

January 2026.

We had an internal use case at Tower: an embedded DuckDB instance, run from C++, serving multi-tenant analytical queries from a single in-memory database. Two missing primitives kept biting us — there was no way to bound the memory budget *per connection*, and no way to time-bound a single runaway query. Both are standard postgres-shaped capabilities. Both were trivially missing.

I sat down to think about what the right shapes for these settings would be. That part — the ideas, the API, the integration story — was mine. The C++ implementation was all [Cursor](https://cursor.sh/), the AI coding agent I use at work. I'm not going to pretend otherwise.

DuckDB has a strict policy against AI-enabled PRs[^duckdb-policy]. So I went the other direction. I broke each patch into small, independently reviewable commits. I reviewed every line myself before pushing.

[^duckdb-policy]: Most serious database projects do, and for good reasons — license cleanliness, code quality, maintainer load. The point of disclosing AI use isn't moral; it's practical. The maintainer's time is the scarce resource. If you're using AI, you owe them an even tighter PR than if you weren't.

Two PRs landed:

- [#20585](https://github.com/duckdb/duckdb/pull/20585) — `max_execution_time`, merged Jan 26, 2026.
- [#20219](https://github.com/duckdb/duckdb/pull/20219) — `operator_memory_limit`, merged Feb 2, 2026.

Both are now in DuckDB main. Both will ship in some upcoming release (we missed v1.5.0's feature freeze). Tower needed them. We're using them. So is, presumably, anyone else who pulls DuckDB and wants per-connection budgets[^duckdb].

It was the first piece of upstream open source code I had merged in a decade. My manager at TRC was fully on board — once we needed it for our system, contributing back was the right thing to do. A decade after Ruaok's IRC message, I had become, finally, a contributor who stuck around long enough to address review feedback.

सितारों से आगे जहान और भी हैं<br>
अभी इश्क़ के इम्तिहान और भी हैं

*(There are worlds beyond the stars —<br>
the trials of love are far from done.)*[^iqbal-1]

[^iqbal-1]: Iqbal. I keep coming back to this couplet whenever I'm tempted to think any one chapter is closed. The trials of love (or craft, or anything you take seriously) keep coming. The stars are not the destination.

## adeeb

I should tell you about my landlord.

When I was 18 and starting BTech at Jamia in 2012, my mom had been renting a single second-floor room in Jafrabad's Gali No. 7 since 2006 — a few minutes' walk from her school. The owner of that house is **Wasim bhai**, a gem of a human being whose family has effectively been ours for two decades. His three kids — Arisha, Uzair (a genuinely talented cartoon artist), and Adeeb the youngest — I have watched grow up in front of me. Adeeb is now in his second year of BTech CS.

I have been pestering him for months: *give GSoC a shot. You're a CS student in 2026, you have time, you have AI agents, you have me.* This year, finally, he took it seriously.

We started at MetaBrainz, of course — the obvious choice for a kid I was mentoring with my own history. He picked [ListenBrainz](https://listenbrainz.org/), which is the MetaBrainz family's Last.fm-style listening tracker.

His first PR — [#3536](https://github.com/metabrainz/listenbrainz-server/pull/3536), a small fix to the fresh releases range selector — went in clean. AI-assisted but tightly reviewed by Adeeb, merged by [MonkeyDo](https://github.com/MonkeyDo) on Jan 27, 2026. We were thrilled.

His second PR — [#3544](https://github.com/metabrainz/listenbrainz-server/pull/3544), an API endpoint refactor for export — went the other way. Adeeb let Cursor generate the change and we didn't review the diff carefully. Sixty lines of test assertions silently disappeared. The test suite broke. MonkeyDo asked, on Jan 30:

> *Initial review, there are some dubious changes that I can't explain to myself. If you generated the PR with AI, you must disclose it. I will point you to our [AI usage policy](https://github.com/metabrainz/guidelines?tab=readme-ov-file#ai-use-policy).*

When Adeeb confessed two weeks later, MonkeyDo's reply:

> *I will point you to our AI use policy, you must disclose any use of AI (and before we catch you in the act, not after). A piece of advice: don't trust AI output, it makes you a worse developer. Use your own skills, make sure you test your changes and review everything twice.*

A few days later: *"LLM slop PR, closing."*

It is the same MetaBrainz, ten years later, holding the same line. The slur has changed — "drive-by contributor" has become "LLM slop" — but the discipline is identical. *Don't waste maintainer time. If you're going to use the help, take responsibility for the result.* And both times, the kid being told this is an Indian college student trying to use the program as a leg up.

The mirror is uncomfortable to look at. It is also the most honest thing I can show you.

We pivoted. We looked for orgs that were selected for GSoC 2026 for the first time, so the candidate pool would be smaller. Adeeb has now submitted proposals to [Wagtail](https://wagtail.org/) (the CMS) and [Learning Unlimited](https://learningu.org/) (an education non-profit). As I write this, he is patiently waiting for the results.

I genuinely do not know if he will get in. If he does, he will do it with a fraction of the activation energy I needed in 2014, because tools like Cursor make it possible for a 20-year-old in Jafrabad to draft a substantial PR over an evening — *if* he applies his brain to it. Which is exactly what [Google's GSoC 2026 AI guidance](https://developers.google.com/open-source/gsoc/resources/ai_guidance) is now warning organizations to require[^google-policy].

[^google-policy]: Google has, for the first time, asked every GSoC org in 2026 to publish a clear AI usage policy. The guidance distinguishes between using AI for research and learning (encouraged), boilerplate and grunt work (encouraged), and core logic that the contributor doesn't fully understand (discouraged, sometimes outright banned). The mentor concerns it summarizes are exactly what MonkeyDo was venting on Adeeb's PR: low quality, blind trust, hindrance to learning, increased maintainer load. Read the [page](https://developers.google.com/open-source/gsoc/resources/ai_guidance). It's the most honest summary of where the OSS-AI tension is right now.

The structural barrier mutates. In 2014 we needed *money* to contribute. In 2026 we need *permission* — and the sense — to use the tools that lower the cost of contributing. The barrier doesn't disappear. It just changes shape.

मोहब्बत मुझे उन जवानों से है<br>
सितारों पे जो डालते हैं कमंद

*(My love is for those young ones —<br>
who throw their lasso at the stars.)*[^iqbal-2]

[^iqbal-2]: Iqbal again. If there's a single line that captures what I want from Adeeb, and from Ziqra, and from whichever Indian undergrad reads this post and decides to apply to GSoC 2027 — it is this. *Sitaaron pe daalna kamand.* Lasso-throwing. Audacity. Even when you miss, you've built the muscle for it.

## the hope

The post should end here, but I have some private dreams I want to leave on the page.

**Iqra**, my mamu's eldest daughter — nickname *Muskan*, "the smiler" — just got into MBBS at HNB Uttarakhand Medical University. The first time I held her was July 2005, a few days after she was born, and I fell in love with how cute she looked on the spot. Allah has, by some accounting I do not understand, kept that cuteness in good repair ever since.

![Iqra at our desk in Gurgaon, July 2009](/images/Muskan-PC-20090719.jpg)

*(That CRT and that desk in the background — same desk Mehtab and I were sitting at in the photo at the top of this post. Half my childhood happened in front of that screen.)*

**Ziqra**, my mamu's second daughter — technically my cousin, but on most days she feels more like my sister, and on her best days like my own daughter[^ziqra] — just gave her BTech entrance exams. She wants to do CS or AI. I am going to push her toward open source the same way the elders pushed me. Maybe MetaBrainz, full circle. Maybe somewhere new.

[^ziqra]: When my parents separated, our family of four split into four pieces — my dad alone in Noida/Gangavli, my mom alone in Delhi, Mehtab with our nani and Bhaiya mamu in Dhandhera, me with Nadeem mamu and mami in Gurgaon/Bahadurgarh. Mamu's four daughters became, by sheer time-on-floor, basically my sisters. Some days they still feel like daughters. The Indian extended family does this kind of forensic emotional accounting, and most of the time it is a gift.

Ziqra, who has a deeper religious instinct than I do, immediately heard *open source contribution* and mapped it to *sadqa-e-jariah* — the Islamic concept of perpetual charity, the kind that keeps giving long after you are gone. A piece of code people use after you're dead, she said, is a kind of prayer. *(That is its own post for another day.)*

**My brother Mehtab.** Guddu has done everything I dreamed of doing. He did a [GSoC with XBMC/Kodi in 2018](https://blog.mzfr.me/), then GSoC with Honeynet on [SNARE/TANNER in 2020](https://www.honeynet.org/2020/11/13/gsoc-2020-project-summary-snare-tanner/), and came back as a Honeynet mentor afterward. He finished his master's at NUS and is now starting his PhD there in the [Trustworthy and Secure Software lab](https://nus-tss.github.io/team/), after a stint at NUS's TEST Lab on his master's dissertation. Somewhere along the way he also picked up an OSCP, an eJPT, and bug-bounty Hall-of-Fame entries at GitHub, PayPal, and Google[^mehtab]. He writes some of the best [security blog posts](https://blog.mzfr.me/) I read.

[^mehtab]: He doesn't publicize this stuff much, so I am going to be the embarrassing older brother and do it for him. The full list is on his [about page](https://blog.mzfr.me/about/).

**My future kids.** Family is a thing I am thinking seriously about this year. If I'm lucky enough to have children, I would love for one of them — even one — to grow up and contribute to MetaBrainz. Half-joking, half-not. Every father wants his progeny to carry his loves forward. This is mine.

**Travel.** The day I get to travel Europe properly, the [MetaBrainz office](https://metabrainz.org/team) — wherever it is currently centered — is on my list. I'd like to  shake the hands of the people who paid for my mother's loan, even if they don't remember me.

**Other projects.** [KDE](https://kde.org/) deserves a sentence. I daily-drove KDE for three or four years and was floored by the quality of desktop they ship as volunteers. My C++ wasn't strong enough then to contribute. Maybe one day. There are a hundred volunteer-led projects — Wikipedia, Debian, Mozilla, Inkscape, OpenStreetMap — that hold up large parts of the digital world without anyone making them. I don't have the right words for the respect I feel toward people who do that work for free, year after year.

**The debt.** Career-wise, I am what I am because of open source. Three GSoC stipends opened doors I couldn't have walked through otherwise. The work I did on Picard and CritiqueBrainz and Mitmproxy taught me what production code looks like, what code review looks like, what a well-run community looks like. Every job I've had since has been a derivative of that summer in Dhandhera at 3 AM with the MTS dongle.

I owe these projects something. I have to pay it back somehow.

## end

*Qarz-e-Hunar* means **the debt of craft**. The debt you owe the people and projects that taught you how to make things. The debt you can only repay by making more things — and by helping someone else start.

It is, gratefully, not the kind of debt my mother feared. It does not stand against a salary, and it does not compound. It is the kind of debt you pay back in PRs, in mentorship, in time you make for a neighbor's kid, in small comments on someone else's IRC channel at 3 AM.

---

Aaron Swartz, on a stage in the sun, microphone in hand: *programming is a superpower.*

A boy in Gurgaon Sector 5, hunched over a desktop with his little brother, downloading a stranger's video on a pendrive that cost him ten rupees an hour.

Both of them are still here. Both of them are still listening.
