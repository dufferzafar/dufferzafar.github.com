---
layout: post
title: "Fixing mnemonic not found bug in Sublime Text"
date: 2015-06-16 04:25:14 +0530
comments: true
categories:
---

I was using the Sublime's built in console (accessed by <code>Ctrl+`</code>) to perform some calculations when suddenly my console got filled with some weird warnings.

<!-- more -->

```
warning: mnemonic n not found in menu caption Cut
warning: mnemonic w not found in menu caption Word Wrap
warning: mnemonic n not found in menu caption Cut
warning: mnemonic w not found in menu caption Word Wrap
warning: mnemonic b not found in menu caption Bookmarks
warning: mnemonic t not found in menu caption Tools
warning: mnemonic c not found in menu caption CSV
warning: mnemonic w not found in menu caption Word Wrap
warning: mnemonic w not found in menu caption Word Wrap
warning: mnemonic b not found in menu caption Bookmarks
warning: mnemonic t not found in menu caption Tools
warning: mnemonic c not found in menu caption CSV
```

If this wasn't a boring day, I would've just let them be. But it is. So...

Googling 'mnemonic not found sublime text' took me to this issue: https://github.com/wbond/package_control/issues/891

The issue has a link to this fix: https://github.com/Monnoroch/ColorHighlighter/pull/216

Now, what do we know? The warning is generated when Sublime can't find literally find the mnemonic in the caption. Hmm, this should've been clear from the start.

How do we fix it? We change the mnemonic to something that Sublime can find in the caption. Damn straight!

We do know from the pull above that this is coming from a `.sublime-menu` file, But still have no idea what plugin is causing this.

We also know where all sublime packages are kept. `~/.config/sublime-text-3`

Let's see if we can search some text in all the of these menu files:

``` bash
find . -name "*.sublime-menu" -exec grep -H 'mnemonic\": "w"' {} \;
```

I found out a bit later that we can do [better](http://unix.stackexchange.com/a/131546) than that - recursive greppin!

``` bash
grep -R --include="*.sublime-menu" "\"mnemonic\": \"w\""
```

I opened the files that looked fishy by passing them to [fpp](https://github.com/facebook/PathPicker), which has only just got the ability to [search sublime config files](https://github.com/facebook/PathPicker/issues/144).

Fixing the actual bug was as easy as changing the case of the mnemonics.

I still have two warnings (t in Tools & c in CSV) that are still not fixed, I guess they are coming from a menu file kept in some `.sublime-package`

For that I'll have to search compressed files. Interesting, but I'm tired and it's [5'o clock in the morning](https://www.youtube.com/watch?v=noLrCDzAp5M).
