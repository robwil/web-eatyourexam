---
author: rob
categories:
- Optimized Firefox
date: "2007-05-31T20:39:08Z"
guid: http://eatyourexam.com/?p=94
id: 94
title: G3-Optimized Firefox 2.0.0.4
url: /?p=94
---
UPDATE (06-04-07): I knew I wouldn’t get this done any earlier than Sunday. So, here it is. Mozilla Firefox 2.0.0.4 optimized for G3! Click [here](http://eatyourexam.com/my-files/ff-opt/firefox-2.0.0.4.en-US.mac.dmg "Firefox 2.0.0.4 G3-Optimized Download") to download it.

If you are interested in hearing my excuse as to why this is so late, click the link below (or if you are viewing the post directly [not from the home page], then just read below).  
<!--more-->

I just want to say that I am aware that Mozilla Firefox 2.0.0.4 was released yesterday. It showed up on my Windows auto-update after 5 p.m. Anyway, the reason I have not yet released the G3-Optimized build (I’ve been previously pretty good at doing it on the first or second day) is because my G3 iBook is sort of acting up.

To make a long story short: for some unknown reason, some of my Unix binary files were corrupted, and when I run them they give me an error that says “Malformed Mach-O file”. What that means is that I would have to reinstall those programs. Easier said than done, unfortunately. Most of these were installed with the Mac OS when it was installed, and thus I can’t easily reinstall them without reinstalling everything. Also, others were built from source code, and finding the same version of the source code and then recompiling everything could take a while.

What does all this have to do with my builds? Well, it turns out that one of the malformed files is rsync, the popular synchronization app for Unix. Countless businesses use it to backup their clients and servers, and Mozilla uses it during the build process of Firefox. So, until I get rsync fixed up, I cannot build 2.0.0.4. It shouldn’t be a major set-back, but I have a lot of things going on such as SATs and bogus History projects, so I probably won’t get to this until Sunday (late Saturday night at the earliest).