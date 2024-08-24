---
title: Finding files faster than your friends
date: 2021-10-28 13:37:21
draft: true
---

## Outline

We begin with the GNU family of tools (`ls`, `tree`, `find`, `grep`) and their hipster cousins (`exa`, `fd`, `rg`)

* The GNU family
    * ls
        * https://lib.rs/crates/ffcnt
    * tree
    * git ls-files
        * https://cj.rs//blog/git-ls-files-is-faster-than-fd-and-find/
        * [HN Discussion](https://news.ycombinator.com/item?id=29298017)
            * How could we create an everything clone on Linux?
            * https://github.com/rflament/loggedfs
            * https://en.wikipedia.org/wiki/Log-structured_file_system
    * find
    * grep

* Their rusty cousins
    * [exa](https://the.exa.website/) / lsd
    * fd
    * rg + hgrep, ugrep

* Indexed search
    * Everything on Windows/NTFS
    * Everything for ext4

    * The locate family
        * rlocate & its kernel shenanigans
        * [lolcate-rs](https://github.com/ngirard/lolcate-rs)

    * `loki`: our own custom locate tool
        * Julia's [post](http://jvns.ca/blog/2015/03/05/how-the-locate-command-works-and-lets-rewrite-it-in-one-minute/), [twitter discussion](https://mobile.twitter.com/b0rk/status/573518446433992704)
        * fd, rg, bat, fzf


* Code search
    * ctags
    * LxR: https://lxr.sourceforge.io/en/index.php
        * LxRng
