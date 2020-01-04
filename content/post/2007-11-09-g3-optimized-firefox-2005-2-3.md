---
author: rob
categories:
- Optimized Firefox
date: "2007-11-09T23:40:51Z"
guid: http://eatyourexam.com/?p=103
id: 103
title: Intel-Optimized Firefox 3.0 Beta 2 for Leopard
url: /?p=103
---
I have been having a lot of problems with Firefox on Leopard. Basically, it would work OK for a little bit but then slow to a crawl. It turned out the memory usage was getting out of control. The Firefox process was using 1.5GB at one point, which was all available space. I guess it had some serious memory leak. Either way, it was unusable. I also happen to hate Safari, so I needed to solve the problem.

So, I decided to do what I always do when Firefox doesn’t work nicely for me: build it myself from source. I loaded up the Terminal (which looked a lot cooler with the Red Sands theme that is one of the many options in the Leopard version) and used CVS to pull the latest Mozilla source code. The reason I went with the latest and not the 2.0.0.9 stable release is because I had gotten used to 3.0, and can’t go back. It’s just nice to have the cocoa widgets; the page tagging is also a great feature. (Before Leopard, I was using [El Furbe’s builds](http://firefoxmac.furbism.com/). His nightly Intel builds simply save a lot of time.. you get the latest without having to spend 30 minutes every day rebuilding the latest sources. Anyway, that’s where I got introduced to the awesomeness that is Firefox 3.0.)

The result is Firefox that works well under Leopard. It is optimized for Intel as well. If anyone with an Intel box and Leopard wants a good working version of Firefox, this build should do the trick until El Furbe starts doing Darwin 9 builds, or until Mozilla gets its act together with it’s stock builds. Without further ado, here is Mozilla Firefox 3.0b2 optimized for Intel! Click [here](http://eatyourexam.com/my-files/ff-opt/firefox-3.0b2pre.en-US.mac.dmg "Firefox 3.0b2pre Intel-Optimized Download") to download it. Click [here](http://www.squarefree.com/burningedge/2007/11/06/2007-11-06-trunk-builds/) for The Burning Edge blog which has release notes for the trunk builds.