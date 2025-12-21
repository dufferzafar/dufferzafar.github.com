---
title: Is India Great?
date: 2019-06-21
---

## Prologue

I was chatting with my younger sisters (cousins; 7th & 9th class) and trying to explain why the Preamble to the Constitution of India was in their NCERT Mathematics textbooks.
I tried to say one thing or the other, but just couldn't get my point across.
Being an appreciator of the Socratic method, I stopped talking and just asked them what they thought "India" was, and as they tried to explain it, one of them said "India is a great country!"

---

## Duh!

I don't 'really' know what "great" means. I could probably just Google it to see how lexicographers have defined the word (as I do gajillions of times a day), but if one of my sisters ever asked me ki "bittu bhaiya, great ka matlab?" toh I won't embarrass myself by Googling it, and probably just answer "bada"[^1] since my 'linguistic neural network' remembers the first two usages of the word "great" in "the great hall" (ala Harry Potter) and the "the great wall of china", both of which have the connotations of "bada".

*Assuming* that great does indeed mean 'bada', is India a great country?

Duh!

Beware: "object oriented programming" and a *swad-anusar* sprinkling of "abstract algebra" lay beyond this line.

---

Consider a class *Country* which currently has 195 objects[^2] - "India" being one of them.

Now, to be able to compare two objects of a class, you would have to define a comparator function[^3] that takes in two objects as an argument and returns either -1, or 0, or 1 depending on whether the first argument is smaller than, equal to or larger than the second.

So to be able to compare India with any other nation, we require such a function. 
Under the simplistic assumption made above, I could pray to the Python-gods and come up with a method that just compares the area of the two countries and be done with it.

We could also come up with a notion of "great"-est. 
This brings us to something called a "total order".[^4]
Which is just a fancy way of saying that all objects of a class have to be comparable to each other.
It was hard for me to understand this at first, because I couldn't come up with classes where this wasn't true.[^5]
Once all objects indeed are comparable, and a "trichotomous relation"[^6] has been defined, only one object of the class can be the "winner". I leave the formal proof as an exercise to the reader.[^7]
Only *one* of them can have the largest area in our case.
And that country is the "greatest".

---

When my sister used the sentence "India is a great country" she did not mean that "India has the largest area". Not even close. 
Kids say things that they don't mean all the time. 
Let me just say - all of us use words that we don't really know the meanings of.
We think we do, but as Socrates made it abundantly clear, sometimes, we don't!

Anyway, what do people mean when they say "India is a great country"? 
Well, I don't know. Nobody ever told me![^8]

Maybe, some official document says 'India is great', and I'm just not aware of it?[^9]
Well, the Preamble is a short read - let's check it real quick. 
Hm, so, it does use lots of words to describe something about India but there's not mention of "Great" anywhere. What a shame. I'd be happy if the first line was just "We, the people of India - a great country, have solemnly ..."
My search could just end there. But it doesn't.

Should I go through all the documents myself? 
Wouldn't it be nice if people could just say what they actually mean.

If I ever continue writing this, I'll talk about what "India" means to me.
If I could, I would just tear open my chest, and let people read it off my heart, but hey, I'm no god. Only a human. 
Allah did bless me with words however. I can try to put them to a good use and define *my* "India" or perhaps just fail at it miserably.[^10]

## Appendix: Reputation

When everyone considers you to be a "good guy" and you have a good reputation in social circles that matter to you, 
it is absolutely necessary that you keep your mouth shut, because things can only go downhill for you. 
Just keep your head low, do what you like, don't be "bad" to others and all will be fine.
You just cannot afford to speak up openly, because someone *is* going to take offence, and your rep score will be worse off.

You know how you SHOULD keep your mouth shut? 
Furthermore, You MUST NOT write anything down![^11]
For the written word is very easy to take down, because it isn't human, it doesn't have a face or other features that someone could possibly admire and think before beginning their attack.
You might have moved on since you wrote those words and may no longer even hold those views (or perhaps you never did?[^12]) 
But hey, come on now, people don't care about that shit. 
The words are still there for them to tear apart, and if god forbid you'd written about something that people actually cared about, the cutey-cute internet will ensure that it stays up forever, and people keep reminding you of it.

It's not all bleak though, you can still talk to your close friends who won't judge you. 

When you do have to express yourself in public, prefer to use quotes said by people who the society has already certified great. If your quote can be laid on an image of a person, that's even better. And you know the icing on the top? The person on the image does not even have to be who actually said the words. How amazing is that![^13]
Just take an image of a person, put a quote right next to it and broadcast it out to the world.
Congratulations, you've just made yourself heard while also ensuring that the author of the quote takes the fall for you, which is alright if the person is already dead, right?[^14]

You know what works better than English quotes? Urdu shers! 
If someone can't even pronounce them, how are they even supposed to feel them. 
No feelings, no ad-hominems!

/s

## Appendix: Passion

I saw some videos of Karan Johar doing pre-release promotions for a movie. 
He said that the entire script came to him on a long flight, and he was just sitting there trying to process it all and it came to him with such force that as soon as he landed he locked himself in a room to write it all down.

I found it so relatable. This had happened to me as well you know. It's an amazing feeling to realise that there are other people in this world who do the same batshit crazy stuff that you do and feel the same emotions.[^15]
I still remember the ten-hour stretch in which I wrote ["What To Watch"](https://github.com/dufferzafar/what-to-watch/)
I was in Roorkee; sitting on a sofa, infront of a giant desert cooler.[^16]
It was GSoC season and I had deadlines to meet on the project, but who likes their "work"?
I didn't start coding because it would bring me money or anything. It was the only expression of art I knew! 
Painters paint. Hackers hack.
And that day, I hacked away! I knew while I was writing the script that I'll never use it again, so the code didn't have to pretty or anything. It just had to work, so I could push it to GitHub, get it out of my head and rest with peace.

Quentin Tarantino said in an interview that what makes him proud is not the end product, but knowing that there was a day when the script didn't exist. The paper was blank that morning, and today it isn't. 

When I opened Sublime[^17] at 8:15 am today after only having slept 3 hours, this file did not exist. 

But now it does! 

If that isn't magical, I don't know what is.

## Appendix: Footnotes

[^1]: Let's just hope that she is busy enough to not ask me the difference between big, large, great, greater, greatest

[^2]: Including the 2 non-member observer states in the UN

[^3]: The *cmp* argument in Python's sorted() function

[^4]: When I met ILFP for the first time (which was half-way down the semester) I knew I was at the right place in IIT. All those symbols, they spoke to me, "you can try as hard as you want and we shall remain beyond your reach." "Child, It will take you more than a week of casual reading to understand us", they said to me. And yet, there were people in the same class who used to blow it out of the park. Which used to anger me then, but now (when things turned out to be okay) just comforts me. It was okay to be an absolute shit-show at something, while still doing good in others.

[^5]: If you want to discuss this a bit more; *please* ping me.

[^6]: This is me just trying to point to the gatekeeping inherent in mathematical terms. They can scare away any sane person. The trichotomotu dionsaur is just our comparator function - *cmp* arg in *sorted()*

[^7]: Please write the proof, light it with a matchstick, and flush it down the drain. Kareena Kapoor style!

[^8]: Coz I've never discussed this with anyone but a close friend. And close friends form a !

[^9]: It'd be great (pun?) if we could all just use citations in every statement we make. Something like: "India is a great country. [1]" and then add a ton of references at the end of the paragraph. The world would be a better place.

[^10]: To define is to limit.

[^11]: Please see this for a definition of the words should/must https://tools.ietf.org/html/rfc2119

[^12]: Imagine Socrates is Hulk and dabbing infront of you right now.

[^13]: Who even knows (or cares about) the original author. Historiography is hard, and History was a boring subject anyway. Fuck that shit.

[^14]: You can prefer to sample it from the set of all "good looking females" and then it hardly even matters what the text is. Another life pro-tip, huh?

[^15]: Nerdfighter forever!

[^16]: As I write this, my brother is probably sitting in the same room, infront of the same cooler. Boy, am I jealous!

[^17]: I switched to VS Code after writing the first line as I realised this had to be in Latex - I can see Knuth (looking like Hulk) dabbing infront of me. Even though I chuckle, I'm really scared. I tell him to not do that, "you could end up breaking a bone" I say. The thought of "The Art of Computer Programming" remaining unfinished forever crosses my mind. I Shudder.

