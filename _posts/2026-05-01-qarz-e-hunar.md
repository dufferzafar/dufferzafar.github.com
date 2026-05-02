---
title: "Qarz-e-Hunar"
date: 2026-05-01
---

We didn't have internet at home.

So after school, I'd walk down to the cybercafe near our house, hand the man behind the counter a ten-rupee note (twenty when I felt rich), plug in my pendrive, and start scraping. Wikipedia pages, programming tutorials, conference talks, PDFs — whatever caught my eye that week. I never actually watched anything inside the cafe; I was greedy with the bandwidth. The real treat was carrying it all home and going through it slowly at the family desktop, where my younger brother [Mehtab](https://blog.mzfr.me/) — Guddu — would come visit during his school holidays and we'd sit there hunched together, learning whatever we could.

![Me and Guddu at that desk, August 2010](/images/Shadab-Mehtab-20100812.jpg)

It was on one of those afternoons that I clicked open a video I'd downloaded the day before. A young man in his twenties stood on a stage in the sun, microphone in hand, telling a crowd: *programming is a superpower. It's meant to change the world.*

His name was Aaron Swartz.

I was eighteen, I had been thinking about computers all my life, and here was someone on the other side of the world — dressed nothing like a teacher — telling me that the thing I'd been quietly doing with my hands actually mattered. I don't think I have the right word for what that meant to a kid in Delhi in 2011. The closest I can get is *permission*. Permission to take this seriously.

<!-- more -->

## tl;dr

*Qarz-e-Hunar* is Urdu for **the debt of craft** — what you owe the people and projects that taught you how to make things.

I owe my career to open source — to MetaBrainz mostly, and to three Google Summer of Code summers between 2014 and 2016 that paid me more than my mother earned from a decade of teaching school.

I was also exactly the kind of "drive-by" Indian contributor that maintainers like [Robert Kaye](https://blog.metabrainz.org/author/ruaok/) and [Maximilian Hils](https://news.ycombinator.com/item?id=14020814) complained about on IRC and Hacker News. I left when the stipends did. For the ten years that followed, I was somebody else's cautionary tale.

A few months ago two of my patches landed in DuckDB, and my neighbor's son [Adeeb](https://github.com/Dewolf1/) submitted his first GSoC proposal. This post is about the ten years in between — what they cost, what I owed, and what I am trying to pay back.

## the discovery

Sometime in 2013 or 2014, [Richard Stallman](https://en.wikipedia.org/wiki/Richard_Stallman) came to Delhi.

A bunch of us from JMI went — [Shivam](https://shivamrana.me/), me, [Tushar](https://www.linkedin.com/in/tushar-raheja-bbab51118/), maybe [Nikhil](https://www.linkedin.com/in/nickedes/). The talk, IIRC, was at some Delhi University college. RMS shuffled onto the stage with an old laptop that looked silly even by 2014 standards. He was a heavy man, and at some point during the talk his jumper rode up and a strip of belly showed; the kids at the back of the hall started giggling. They had no clue who he was.

I didn't laugh. I sat there enamored, listening to him talk about the GPL, gcc, the four freedoms. On the bus back to campus I wouldn't shut up about him — I think I gave Tushar an entire history of GNU before we'd reached the campus gate. He handed out free FSF stickers that day. I'm pretty sure I still have one in a drawer somewhere.

---

A few months later, Shivam came up to me with a glint in his eye.

> "Bhai ek org hai jo music ka andha data collect karti hai. GSoC karte hain."
>
> *(Bro, there's an org that collects insane amounts of music data. Let's do GSoC.)*

The org was [MetaBrainz](https://metabrainz.org/). I went home that night, found the GSoC ideas page, and got obsessed. We already knew the program existed — [Akif bhai](https://www.linkedin.com/in/akifkhan1/), a senior from Jamia, had done GSoC the year before and was our proof that kids like us could get in.

I applied to MetaBrainz and got in.

My 2014 project was the [MusicBrainz Picard](https://picard.musicbrainz.org/) website — the marketing site that lives at that URL today — plus a feature inside Picard itself: a way to browse and install community plugins from within the app. It was my first real exposure to Python/Qt desktop development. Robert Kaye — *ruaok*, MetaBrainz's founder — ran the org from somewhere in Europe, and the whole community lived on `#metabrainz` and `#musicbrainz` on Freenode. My IRC handle was `dufferzafar`. It still is.

A few weeks in, Shivam read my first batch of IRC messages and laughed the next day:

> "Tu kitna humble hai re." *(How humble you sound, dude.)*

I was confused. Wasn't that just how you talked online?

It took me years to realize I'd been writing on IRC the same way I'd been writing "Respected Sir" at the top of school exams since I was eight. The maintainers we were talking to were used to something terser. They probably read me as overly formal, slightly off, unmistakably Indian. A small friction, but a real one.

## dhandhera

The work that summer happened from my nani's house in Dhandhera, a small village near Roorkee.

A desert cooler blowing heavenly air. Powercuts, naturally. I had an MTS dongle for the internet[^mts] and a Dell laptop I'd bought in my first year of BTech. The family understood I was "working for Google", which was close enough.

[^mts]: I lived on a 7 GB/month prepaid plan. Monitoring bandwidth was critical enough that I [wrote a Linux usage tracker](https://github.com/dufferzafar/netuse) for it, because Networx didn't exist for Linux. 160 stars later, that repo is a strange little artifact of how thin a thread Indian internet hung from in 2012.

My schedule was inverted: bath at 10:30 PM, dinner, then the desk until six in the morning. IRC was busiest from 2 to 4 AM IST, when the Europeans and Americans were online and my mentors were among them. I'd sleep through the day, wake up around 4 PM, mess about for a bit, and start again.

People in the village would walk past our open gate at odd hours and see me hunched over a screen. Some of them asked Guddu:

> "Tera bhai kya karta rehta hai raat bhar?"
>
> *(What does your brother do all night?)*

He didn't always have an answer.

---

By the end of August, Google had paid me ₹3 lakhs[^stipend] for my work.

[^stipend]: GSoC 2014 paid around $5,500 — close to ₹3 lakh at the time. Across three summers (2014 Picard, 2015 CritiqueBrainz, 2016 Mitmproxy) it added up to about ₹10 lakhs.

In 2001, when I was in class 3rd, my mom had taken a personal loan of ₹3 lakhs to buy a small house. After my parents separated, that loan stood against her salary as a Hindi teacher in a government school. It took her 8 years to pay off, and the fear of loans she developed in those years has stuck with all of us[^loan].

[^loan]: There is no shape of post in which I can talk about my mother for the right amount of time. I'll write about her properly elsewhere. The fact this post needs is: she paid back a ₹3-lakh loan over a span of 8 years of teaching school. I made the same number in three months. The exchange rate of effort to money was the most violent thing I had ever felt.

When I received that first stipend, the only number my brain could put next to it was that loan. Three months at the desk had matched ten years of my mother's pay.

## the fall

I came back the next year — 2015 — for [CritiqueBrainz](https://critiquebrainz.org/), a Flask app for music reviews. My mentor was [Roman Tsukanov](https://github.com/gentlecat). I picked the project because Flask was familiar and I wanted something I could ship without learning a new framework. I don't have many specific memories from that summer. It was easy, and I was getting good at this.

---

In March 2016, between summers, Google gave [Chaitu](https://www.linkedin.com/in/chait/) and me $500 each toward a trip to [FOSSASIA](https://fossasia.org/) in Singapore. The rest we arranged ourselves. It was the first time I left India.

[Chaitanya](https://github.com/ichait) was a close friend then — we've drifted since, in the way friends sometimes do. I delivered a [talk](https://youtu.be/JH_tqlnvIaU) (on terminals, of course) at the conference, ate KFC for 3 days, and walked around Marina Bay feeling like the protagonists of a movie I'd only ever watched.

I met [Stephanie Taylor](https://www.linkedin.com/in/stephaniertaylor/), who ran GSoC at Google — the actual person on the other end of the program that had paid off my mother's loan.

![With Stephanie at FOSSASIA, Singapore, March 2016](/images/Stephanie-Singapore-20160319.jpg)

We also met [Mike McQuaid](https://www.linkedin.com/in/mkmcqd/), then at GitHub, who at some point said in passing: *you two should apply.* We took that sentence back to the AirBnB with us. *Job. At GitHub.* It was a pipedream, and we knew it, and we kept saying it anyway.

The trip split our paths. Chaitu fell in love with the city, did his master's at NUS a few years later, and settled there for good. I came home with a different feeling — *ye pardes bilkul waisa hi hai jaisa mummy ne samjhaya tha.*[^pardes]

[^pardes]: *This foreign place is exactly what mummy had warned me about.* Hindi cinema has a century-long argument about *pardes* — that it looks beautiful from a distance and hollows you out from the inside. Singapore decided it for me in five days. Some people are made for elsewhere. I am very much not.

---

I applied for a third GSoC with MetaBrainz. By that point I'd been on `#metabrainz` for two summers, but my contributions had been almost entirely seasonal — turn up in March, ship through August, vanish till next March. Robert (ruaok) had noticed.

While I was discussing prospective GSoC ideas for the year, ruaok sent a message that, paraphrased from memory, went something like:

> *Shadab, we're not going to take you this year. You only show up for the GSoC period and then disappear, which is against the spirit of the program. If you stick around as a non-GSoC contributor for the year, we'll consider you next time.*

[Aditya](https://github.com/kwikadi), another close friend, was on the channel at the time and immediately started DMing me damage-control advice. *Don't tell him this is your final year. Don't say you won't be a student in 2017. Just nod and say you'll stick around.*

I told him exactly that.

> "Hey Rob, this is my BTech final year. I won't be a student next year."

I felt a little shamed. I tried to weave my way out of it, and couldn't. ruaok had drawn the line cleanly, and I had walked across it onto the wrong side — on public IRC, in front of everyone.

GSoC had become a competitive sport for me by that point, and I did what any half-decent athlete does after a loss: I pivoted.

I applied to [Mitmproxy](https://mitmproxy.org/) under the [Honeynet](https://www.honeynet.org/) umbrella, and got in. My mentor was Maximilian Hils. I made a bunch of scattered improvements that summer, beginning with the Python 2 to Python 3 port of Mitmproxy's major internal libraries.

I lurked around the project for a few months afterward. I never contributed to Mitmproxy again.

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

Here's the thesis.

Open source as it's practiced in the West assumes a social safety net and a career ladder that doesn't punish you for unpaid summers. Indian students don't have that. Cut-throat competition starts in school and only intensifies through college — the population curve is what it is, unemployment is what it is, and we spend our twenties trying to outpace each other because that's the only path through.

Our 2010s GSoC generation showed up for the stipend, learned real craft, then vanished into jobs that demanded everything we had — exactly the pattern Ruaok and Max named on IRC and HN. They weren't wrong. I was one of those students.

And I wasn't alone.

- Shivam, who introduced me to MetaBrainz, never did GSoC. He went on to do excellent work elsewhere, but the open-source hobby never picked up.
- Akif, who had been our inspiration, did his one GSoC at OpenSUSE in 2013 and, as far as I know, didn't go back. I owe him a great deal regardless — without him, I wouldn't have known the program existed.

It wasn't that we didn't want to. I wanted to keep contributing — I genuinely did. But you finish your degree, you take the job that pays the rent or the loan or both, and college courses and exams give way to OKRs and on-calls. The incentive evaporates. The maintainers in Berlin and Amsterdam and Barcelona keep going because their lives have room for it. Ours don't.

This isn't an excuse. It's an explanation.

## the crater

Between 2016 and 2026 there is a ten-year hole in my open-source life.

I joined Adobe straight out of Jamia in July 2016 — a sweet placement, a fat package, a famous company. The role turned out to be writing Selenium-based unit tests in Python. After two weeks of staring at it, I decided a 12th-pass kid could do this work. Over lunch, my friend [Prerit](https://www.linkedin.com/in/prerit2010/) and I quietly agreed to resign together and prep for GATE. My manager was furious:

> "I'll make sure you're blacklisted from Adobe."
>
> "Adobe has invested so much in you already. Is this how you repay?"

That word — *repay* — has stuck.

Adobe held me to a few months of notice. I served it while quietly finishing my Mitmproxy GSoC on Adobe time. For most of that summer, both Adobe and Google were paying me at once — one for Selenium tests I wasn't writing, the other for Python 3 code I actually was.

I gave GATE in February 2017 — AIR 59 — and joined IIT Delhi MTech CS in June. The course load was brutal, and I realised fast that I would have to give up hobbyist programming if I wanted to do well in MTech. As much as it pained me, I did. From 2017 to 2019: almost no hobby OSS. In June 2019 I got placed at [Tower Research Capital](https://www.tower-research.com/), where I have been ever since[^trc].

[^trc]: TRC is a quantitative trading firm — low-latency C++, custom file formats, in-house storage engines. The day job is intellectually rich and it pays absurdly well. I've written elsewhere about the [moral dissonance](/2025/saarthi/) of working in HFT and the [career path that didn't happen](/2026/civil-service/). What it didn't leave room for, for the longest time, was open source.

So: ten years. A few drive-by commits at most. IRC channels kept buzzing without me, exactly as the mentors had predicted they would.

## the return

January 2026.

A project at Tower needed two primitives that DuckDB didn't ship with: a way to bound memory per connection, and a way to time-bound a runaway query. Both are postgres-shaped capabilities. Both were trivially missing.

I worked out what these settings should look like — what to add, how the API should read, how the new options should integrate with the existing knobs. That part was mine. The C++ implementation was all [Cursor](https://cursor.sh/), the AI coding agent I use at work.

DuckDB has a strict policy against AI-generated PRs[^duckdb-policy]. So I overcompensated. Each patch was broken into small, independently reviewable commits. I made multiple passes over the code myself before pushing, and ran the entire test suite locally before opening each PR.

[^duckdb-policy]: Most serious database projects do, and for good reasons — license cleanliness, code quality, maintainer load. The point of disclosing AI use isn't moral; it's practical. The maintainer's time is the scarce resource. If you're using AI, you owe them an even tighter PR than if you weren't.

Two PRs landed:

- [#20585](https://github.com/duckdb/duckdb/pull/20585) — `max_execution_time`, merged Jan 26, 2026.
- [#20219](https://github.com/duckdb/duckdb/pull/20219) — `operator_memory_limit`, merged Feb 2, 2026.

Both are merged into DuckDB main. They'll ship in the release after v1.5.0. We're using them at Tower; presumably so is anyone else who pulls DuckDB and wants per-connection budgets.

It was the first piece of upstream open source code I had merged in a decade. My manager at TRC was fully on board — once we needed it internally, contributing it back upstream was the obvious thing to do. A decade after ruaok's IRC message, I had finally stuck around long enough to address review feedback.

सितारों से आगे जहान और भी हैं<br>
अभी इश्क़ के इम्तिहान और भी हैं

*(There are worlds beyond the stars —<br>
the trials of love are far from done.)*[^iqbal-1]

[^iqbal-1]: Iqbal. I keep coming back to this couplet whenever I'm tempted to think a chapter is closed. The trials of love (or craft, or anything you take seriously) keep coming.

## adeeb

I should tell you about Wasim bhai.

When I was 19 and starting BTech at Jamia in 2012, my mom had already been living for six years in a single second-floor room a few minutes' walk from her school. The house belongs to **Wasim bhai**, a gem of a human being whose family has, over those two decades, become ours. His three kids — Arisha, Uzair (a genuinely talented cartoon artist), and Adeeb, the youngest — I have watched grow up in front of me. Adeeb is now in his second year of BTech CS.

I have been pestering him for months: *give GSoC a shot. You're a CS student in 2026, you have time, you have AI agents, you have me.* This year, finally, he took it seriously.

We started at MetaBrainz, of course — the obvious choice given my history. He picked [ListenBrainz](https://listenbrainz.org/), the MetaBrainz family's Last.fm-style listening tracker.

His first PR — [#3536](https://github.com/metabrainz/listenbrainz-server/pull/3536), a small fix to the fresh releases range selector — went in clean. AI-written but carefully reviewed before submission, merged by [MonkeyDo](https://github.com/MonkeyDo) on Jan 27, 2026. We were thrilled.

His second PR — [#3544](https://github.com/metabrainz/listenbrainz-server/pull/3544), an API endpoint refactor for export — went the other way. Adeeb let Cursor generate the change, and I didn't review the diff carefully enough. Sixty lines of test assertions silently disappeared. The test suite broke. MonkeyDo asked, on Jan 30:

> *Initial review, there are some dubious changes that I can't explain to myself. If you generated the PR with AI, you must disclose it. I will point you to our [AI usage policy](https://github.com/metabrainz/guidelines?tab=readme-ov-file#ai-use-policy).*

When we confessed two weeks later, MonkeyDo's reply:

> *I will point you to our AI use policy, you must disclose any use of AI (and before we catch you in the act, not after). A piece of advice: don't trust AI output, it makes you a worse developer. Use your own skills, make sure you test your changes and review everything twice.*

A few days later: *"LLM slop PR, closing."*

It's the same MetaBrainz, ten years on, holding the same line. The complaint has changed — *drive-by contributor* has become *LLM slop* — but the discipline is identical: *don't waste maintainer time; if you're going to use the help, take responsibility for the result.* Both times, the kid on the receiving end is an Indian college student trying to use the program as a leg up.

An uncomfortable mirror. But the contest was still on — the deadline was still real, and Adeeb still needed to land somewhere. Same play as 2016: we pivoted.

We looked for orgs that were selected for GSoC 2026 for the first time, so the candidate pool would be smaller. Adeeb has now submitted proposals to [Wagtail](https://wagtail.org/) (the CMS) and [Learning Unlimited](https://learningu.org/) (an education non-profit). As I write this, he is waiting for the results.

I genuinely don't know if he will get in. If he does, he'll have done it with much less effort than it took me in 2014, because tools like Cursor make it possible for a 20-year-old in Delhi to draft a substantial PR over an evening — *if* he applies his brain to it. Exactly the discipline [Google's GSoC 2026 AI guidance](https://developers.google.com/open-source/gsoc/resources/ai_guidance) is asking every org to define[^google-policy].

[^google-policy]: Google has, for the first time, asked every GSoC org in 2026 to publish a clear AI usage policy. The guidance distinguishes between using AI for research and learning (encouraged), boilerplate and grunt work (encouraged), and core logic that the contributor doesn't fully understand (discouraged, sometimes outright banned). The mentor concerns it summarises are exactly what MonkeyDo was venting on Adeeb's PR: low quality, blind trust, hindrance to learning, increased maintainer load. Read the [page](https://developers.google.com/open-source/gsoc/resources/ai_guidance) — it's the most honest summary of where the OSS-AI tension is right now.

The structural barrier mutates. In 2014 we needed money to contribute. In 2026 we need both permission and judgement to use the tools that lower the cost of contributing. The barrier doesn't disappear; it just changes shape.

मोहब्बत मुझे उन जवानों से है<br>
सितारों पे जो डालते हैं कमंद

*(My love is for those young ones —<br>
who throw their lasso at the stars.)*[^iqbal-2]

[^iqbal-2]: Iqbal again. If there's a single line that captures what I want for Adeeb, and for whichever Indian undergrad reads this post and decides to apply to GSoC 2027 — this is it. *Sitaaron pe daalna kamand.* Lasso-throwing at the stars. Even when you miss, you've built the muscle.

## the hope

What follows is personal. These are the reasons I started writing.

**Iqra**, my sister — nickname *Muskan*, "the smiler" — just got into MBBS. The first time I held her was July 2005, a few days after she was born, and I fell in love on the spot. Allah has, by some accounting I do not understand, kept that smile in working order ever since. You'll never catch her crying in public. She has her bathrooms for that.

![Iqra at our desk, July 2009](/images/Muskan-PC-20090719.jpg)

*(Same desk, same CRT as the photo at the top of this post — a lot of my childhood happened in front of that screen.)*

**Ziqra**, another of my sisters — technically my cousin, but on most days she feels more like my sister, and on her best days like my own daughter[^ziqra] — just gave her BTech entrance exams. She wants to do CS or AI. I'm going to push her toward open source as hard as I can. Maybe MetaBrainz, full circle. Maybe somewhere new.

[^ziqra]: When my parents separated, our family of four split four ways across different households. Mehtab grew up with our nani; I grew up with our mamu's family. Mamu's four daughters became, by sheer time spent under the same roof, my sisters. Some days they still feel like daughters. The Indian extended family rearranges itself around things like this, and most of the time it's a gift.

Ziqra has a deeper religious instinct than I do, and made the connection at once: open-source contribution is a form of *sadqa-e-jariah* — the Islamic idea of perpetual charity, the kind that keeps giving long after you are gone. A piece of code people use after you're dead, she said, is a kind of prayer. *(That's its own post for another day.)*

**My brother Mehtab.** Guddu has done everything I dreamed of doing. He did a [GSoC with XBMC/Kodi in 2018](https://blog.mzfr.me/), then GSoC with Honeynet on [SNARE/TANNER in 2020](https://www.honeynet.org/2020/11/13/gsoc-2020-project-summary-snare-tanner/), and came back the next year as a Honeynet GSoC mentor. He finished his master's at NUS and is now doing his PhD there, in the [Trustworthy and Secure Software lab](https://nus-tss.github.io/team/). Somewhere along the way he also picked up an OSCP, an eJPT, and bug-bounty Hall-of-Fame entries at GitHub, PayPal, and Google[^mehtab]. He writes some of the best [security blog posts](https://blog.mzfr.me/) I read.

[^mehtab]: He doesn't publicise this stuff much, so I'm going to be the embarrassing older brother and do it for him. The full list is on his [about page](https://blog.mzfr.me/about/).

**My future kids.** Family is something I'm thinking seriously about this year. If I'm lucky enough to have children, I'd love for at least one of them to grow up contributing to open source — the way I did, the way Mehtab did. Half-joking, half-not. Every father wants his kids to carry his loves forward. This is one of mine.

**Other projects.** I daily-drove [KDE](https://kde.org/) for three or four years and was floored by the quality of the desktop they ship as volunteers. My C++ wasn't strong enough then to contribute. Maybe one day. There are a hundred volunteer-led projects — Wikipedia, Debian, Mozilla, Inkscape, OpenStreetMap — that hold up huge chunks of the internet without anyone making them. I don't have the right words for the respect I feel toward people who do that work for free, year after year.

**The debt.** Career-wise, I am what I am because of open source. Three GSoC stipends opened doors I could not have walked through otherwise. The work I did on Picard and CritiqueBrainz and Mitmproxy taught me what production code looks like, what code review looks like, what a working community looks like. Every job I've had since has been a derivative of that summer in Dhandhera at 3 AM with the MTS dongle.

I owe these projects something. I have to pay it back somehow.

## end

The debt of craft is, gratefully, not the kind of debt my mother feared. It doesn't stand against a salary; it doesn't compound. You pay it back in PRs, in mentorship, in time you make for a neighbour's kid, in small comments on someone else's IRC channel at 3 AM. By making more things. By helping someone else start.

---

Aaron Swartz, on a stage in the sun, microphone in hand: *programming is a superpower.*

A boy at the family desktop with his little brother, picking through a pendrive of cybercafe loot.

The man on the stage is still saying it. The boy at the desk is still listening.
