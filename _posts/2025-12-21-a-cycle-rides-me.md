---
title: A Cycle Rides Me
date: 2025-12-21
---

I was diagnosed with Bipolar in 2021 after a major manic episode following my recovery from the physical symptoms of COVID.

In this post, I present data analytics on my personal data that highlights the effects of / causes & some surprising benefits of being bipolar. We start with a brief overview of what the polarity spectrum looks like & then quickly dive deep into the data and some visualisations.

All of the code used to create this is public here:
- [https://github.com/dufferzafar/bipolar/](https://github.com/dufferzafar/bipolar/)
- [https://github.com/dufferzafar/activity/](https://github.com/dufferzafar/activity/)

## Background

The last 4 years have been a particularly challenging time for me as I've learned to identify triggers / patterns that improve / worsen my disorder.

I'm really grateful to everyone who has supported me through this challenging time. Apart from family, I've been very lucky to have friends around me who take care of me. Some names I'd like to drop are: [Shivam](https://shivamrana.me/) for pinging me and pushing me. [Shreyansh](https://github.com/bk1603) for being an ideal younger brother and [Rachit](https://www.youtube.com/@RachitJain) for always calling.

I wrote these lines some time back:

> कुछ दोस्त मुझे यूँ मिले हैं ऐसे<br>
> गुलाब को गुलदान मिले हो जैसे 

_(Some friends have found me / like a vase finds its rose.)_

I also owe apologies. To people I've hurt - with words, with actions, with silence. Some of it was the disorder talking. Some of it was just me. The line between the two isn't always clear, and I'm not using bipolar as an excuse.

If you're reading this and I've wronged you - intentionally or not - I'm sorry. I'm working on it. I can't promise I won't slip again, but I can promise I'm more aware now than I was before.

To my girlfriend of 7 years — it's been complicated. The lows are probably hardest for her: I disconnect, my pessimism takes over, I start detaching. The highs bring their own pain — endless discussions, false hopes. She's been patient. More than I deserve, probably.

<!-- 
She's been of immense help. She has her own demons and understands mine. We're not broken up. And I intend to marry her — this is not just the mania talking. Or is it?
-->

## Why I'm sharing this now

For 4 years I've mentioned "health stuff" to colleagues and acquaintances without naming it. That ambiguity felt protective but also isolating. I'm tired of the cognitive load of half-truths.

There's also the data angle: I've been tracking myself obsessively since diagnosis, and the patterns are finally clear enough to share. If even one person sees their own experience reflected here—or learns what to look out for—this post will have been worth it.

## What is Bipolar?

Bipolar is a mood disorder, characterised by a boom-bust cycle of elevation and depression. Like all sinusoidal waves, it has both an amplitude and a time period. 

<!-- TODO: Insert chart here. Manic. Hypo. Depression. -->

And yes - the title is a double meaning. I ride an actual cycle too. It's a Hero cycle I got from my elder brother - no gears or suspension. [Premium Rush](https://www.youtube.com/watch?v=Pn6ie1zCkZU) style.
And a carrier. Not a pannier, mind you. A proper - can carry an atta-katta - carrier.

Early morning rides became my cheapest mood regulator: 20 km before sunrise resets whatever the night scrambled. The physical bi-cycle and the mental one are now inseparable in my head.

For me specifically:

**Hypomania** looks like: sleeping 2 hours and feeling invincible, non stop poetry writing, starting 5 side-projects, talking too fast. Praying namaz 5 times a day, trusting the Almighty for all He is doing and will do.

**Depression** looks like: 14-hour sleep, unanswered calls/messages, code that feels pointless, even basics like a bath starts to feel like a chore. And losing faith — not just in myself, but in God too. Hope leaves, and prayer leaves with it.

## It runs in the family

My father was probably bipolar too. And his mother — my dadi — was somewhere on the spectrum. Both took treatment from [IHBAS Delhi](https://en.wikipedia.org/wiki/Institute_of_Human_Behaviour_and_Allied_Sciences).

I don't remember much of my father's bipolar. My mom does. But I do remember once, coming back from IHBAS, he was so low he thought a rickshaw-wala would take us all the way to Noida.

My dadi I remember more fondly. She'd hand me 10 rupees and say — "5 rupees ka tambaku le aana aur 10 rs wapas!"

I always knew bipolar was coming for me. Even at IIT, I had cycles — super low during semester breaks, then "up and at it" once classes started. I just didn't have a name for it yet.

My parents separated when I was 11. My father was abusive towards my mother. Most of those memories are closed to me now — my brain's way of protecting itself, I think. But one image stays: I was 7 or 8, my mother asked me not to leave the house. I left anyway. When I came back, she had a black eye. I can't get it out of my head.

He passed away in 2015, when I was 22. We'd cut all contact by then. He was sick and dying and wanted to meet us — but I didn't believe him. I thought it was another ruse. Part of me regrets that now. Part of me still loves him.

It's hard on my mom too. She sometimes compares my actions with his. It boils my blood — but I get it. How could she not see him in me?

Bipolar has a high genetic component. So does psoriasis — another disorder I've been managing since 2014. I take phototherapy sessions at GTB Hospital, which happens to be right next to IHBAS. Two generations, two hospitals, side by side.

The two conditions feed each other. When I'm depressed, I stop caring about the psoriasis — forget to apply topicals, let it get worse. When the highs come, I rush to doctors and get back on a treatment plan.

My brother, thankfully, shows no signs. He's built a healthy lifestyle I never could — runs daily, finished a full marathon last year. I'm grateful for that.

Both conditions are part of why I want to "solve" this before I die. For him. For my future children. So the cycle — the real one — can end. 

## Modelling the cycle

So, what does a cycle look like? Not a bi-cycle (soft pun?), not a tri-cycle, but the bipolar cycle!

One of my move 37 ideas - a term from AlphaGo's [famous game](https://en.wikipedia.org/wiki/AlphaGo_versus_Lee_Sedol#Game_2), meaning an unexpected creative leap - was to look at this cycle from the lens of [Ray Dalio](https://en.wikipedia.org/wiki/Ray_Dalio) whose work has gone into characterizing Economic cycles.

I'll be writing a separate post on this soon. For those curious, here's [_something_](https://github.com/dufferzafar/bipolar/blob/main/models/Ray%20Dalio.md) to hold you over.

## In the age of AI

When I'm elevated, some of my thoughts can be too crazy for even myself. I've derived huge value from ChatGPT DeepResearch for exploring chains of thoughts that can only come from a human hypo filled haze.

Applying [Taleb's model of fragility to organisational silos](/2024/08/24/silos-and-fragility/) was one such example. I still remember the sigh of relief I breathed when the model confirmed I was thinking in the right direction.

My post on the [parallels between Turing and Swartz's deaths](/2024/10/08/turing-and-swartz/) was another case where the LLM helped me chase a thread I couldn't have followed alone.

## Where am I now

Elevated, again. Sleeping 2-3 hours a night. Currently on lorazepam (sleep aid) and aripiprazole (mood stabilizer), with psych appointments every couple of months.

What's helped most? Meds — especially sleep aids. And exercise to channel the excess energy. The cycling isn't just a metaphor.

What I wish I'd known at diagnosis: how hard it all is. At my highs I have infinite optimism. At my lows, infinite pessimism. After a few cycles of this, it takes its toll.

I'm not fully comfortable talking about how this has affected my work. What I will say is that there are colleagues who stood by me at my times of need.

The data tracking isn't about control — it's about understanding. I'm not concerned with what exists today. I don't want my brother to go through this. Or my children. I'd like to "solve" bipolar before I die, with solid technology. That's who I am.

This post is part of that. I have multiple lenses now — Surah Ad-Duha from the Quran, a spring-mass-damper system, the Dalio model. I'll be sharing these in future posts. The goal is to benefit anyone else going through this.

If you haven't heard from me in a while — reach out. I appreciate it more than you know.
