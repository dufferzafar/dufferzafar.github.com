---
redirect_from: /2017/03/30/system-setup/
layout: post
title:  System Setup
date:   2017-03-30 00:53:11
---

The last laptop I owned was a Dell Inspiron 5520, which I purchased in 2012 for 42k. It was not a great machine by any means but it served me well until one day when it just wouldn't boot. I sold it for ₹ 3500 and decided to buy a new laptop.

After some searching, I settled for the Inspiron 7560. I bought it for 80k a few days ago and this post details how I'm setting it up.

<!-- more -->

The first thing I did after bringing the laptop home was remove the hideous Dell & Intel i7 stickers.

7560 comes with an SSHD setup: 1 TB HDD + 128 GB SSD. Windows 10 is installed on the SSD while the HDD is empty.  

---

When re-installing manjaro, I did not delete my old /home/ folder - as it had all my configuration.

I have a disk setup like:

## Setting up a new system commands

## Manjaro tweaks

* Touchpad
    - Symptoms
        + Some of the settings in Touchpad configuration were disabled before
        + Double click was not working in some GTK applications
            * Sublime etc.
    - Cure
        + Install synaptics driver
        + xorg config
        + Now use the Touchpad settings to set it how you like it

## Issues 

* Broken pip
    - Symptoms
        + Running `pip` was giving this error:

        ```bash
        Traceback (most recent call last):
          File "/usr/bin/pip", line 11, in <module>
            load_entry_point('pip==10.0.1', 'console_scripts', 'pip')()
          File "/usr/lib/python3.6/site-packages/pkg_resources/__init__.py", line 476, in load_entry_point
            return get_distribution(dist).load_entry_point(group, name)
          File "/usr/lib/python3.6/site-packages/pkg_resources/__init__.py", line 2700, in load_entry_point
            return ep.load()
          File "/usr/lib/python3.6/site-packages/pkg_resources/__init__.py", line 2318, in load
            return self.resolve()
          File "/usr/lib/python3.6/site-packages/pkg_resources/__init__.py", line 2324, in resolve
            module = __import__(self.module_name, fromlist=['__name__'], level=0)
          File "/usr/lib/python3.6/site-packages/pip/_internal/__init__.py", line 42, in <module>
            from pip._internal import cmdoptions
          File "/usr/lib/python3.6/site-packages/pip/_internal/cmdoptions.py", line 16, in <module>
            from pip._internal.index import (
          File "/usr/lib/python3.6/site-packages/pip/_internal/index.py", line 25, in <module>
            from pip._internal.download import HAS_TLS, is_url, path_to_url, url_to_path
          File "/usr/lib/python3.6/site-packages/pip/_internal/download.py", line 48, in <module>
            from pip._internal.utils.ui import DownloadProgressProvider
          File "/usr/lib/python3.6/site-packages/pip/_internal/utils/ui.py", line 11, in <module>
            from pip._vendor.progress.bar import (
        ModuleNotFoundError: No module named 'pip._vendor.progress.bar'; 'pip._vendor.progress' is not a package
        ```

        + `sudo pip` was working just fine.
        + I don't really know why
        + Copied my libs from older installation: `~/.local/lib/python*` 

