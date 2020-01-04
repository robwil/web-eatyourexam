---
author: rob
categories:
- Optimized Firefox
date: "2006-10-28T14:54:27Z"
guid: http://eatyourexam.com/?p=66
id: 66
title: Firefox 2.0 Optimized for Mac G3
url: /?p=66
---
Neil over on [now up](http://www.beatnikpad.com/archives/2006/10/26/firefox-20) on his blog. There are many people who swear by his optimized builds and claim they yield a major speed increase. However, there is one little problem&#8230; he only offers builds for G4, G5, and Intel processors. That leaves me and my iBook G3 700mhz stuck without any optimization. So, what to do?

I decided to make my own optimized build. Firefox is an open source browser, so any old person can go download the source code. They have scripts that make it easy to build, so all you really need is a good development environment (meaning you have Perl, GCC, etc., which OSX users can get with the Developer Tools included on the Tiger DVD) and enough time to let it compile. Compiling the libIDL, which is a prerequisite for Firefox compilation, took about three hours. Firefox then took about five. The good part is I will only have to go through the five-hour process next time, since libIDL is already on my system.

To spare anyone else from going through the eight-hour process, I used the friendly installer-maker script to create a compressed dmg file ready for download and use. Keep in mind that this will **only work on G3 processors**. Without further ado, you may click [here](http://eatyourexam.com/my-files/ff-opt/firefox-2.0.en-US.mac.dmg) to download Firefox 2.0 Optimized for G3 processors.

**Note:** During the build process, I did come in contact with one little issue. However, the Firefox developers helped me resolve it quickly. The error I got was &#8220;&#8216;kCGBitmapByteOrder32Host&#8217; undeclared&#8221; in the file mozilla/gfx/cairo/cairo/src/cairo-quartz-surface.c. The developers informed me that in the header file for the problematic source file, there were three particular lines that checked to see if the SDK installed was version 10.4 or higher. If so, it did nothing. However, if it was a lesser version, it would define the kCGBitmapByteOrder32Host constant to 0. This is because Tiger implements the constant somewhere on its own, and doesn&#8217;t need the Firefox source code to do it. For whatever reason, my system registered as 10.4 or higher (I am using Tiger), but did not have that constant defined by the OS, and therefore errored out since it wasn&#8217;t defined by anything. I fixed this by commenting out the if statement in the header file so the constant would be defined as 0 for my system as well.

For those interested in a more technical representation of what I did, [here](http://eatyourexam.com/my-files/ff-opt/cairo-quartz.h.diff) is the diff file between the original and patched version of cairo-quartz.h.