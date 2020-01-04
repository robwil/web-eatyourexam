---
author: rob
categories:
- Tech
date: "2011-06-10T00:50:47Z"
guid: http://eatyourexam.com/?p=116
id: 116
title: Very Strange Computer Problem
url: /?p=116
---
I had a really weird computer problem today, and I figured I would share the symptoms and solutions, since it took me about 4 hours to finally find the answer through Google. Hopefully this posting will get picked up by Google and help anyone else with a similar problem out.

**Symptoms:**

My laptop computer is usually plugged in to the AC power, my USB mouse, and my ethernet cord. Whenever I use it at the kitchen table, for instance, I unplug all three of those things and move it. Usually this works perfectly, with no issue whatsoever. However, two days ago this is what happened. When I would unplug my computer, it would become extremely sluggish within a few seconds and stay that way until I plugged it back in again.

I determined the cause of the sluggishness was 100% CPU usage (as opposed to high disk activity or RAM exhaustion), but this didn&#8217;t help determine the root cause because the culprit process was &#8220;System&#8221;, which isn&#8217;t exactly something I can uninstall or stop from running, as it&#8217;s integral to the Windows OS. I should also note some other symptoms. Every 30 seconds or so in this &#8220;sluggish&#8221; mode, the computer screen would turn black and come back a few seconds later &#8212; it turned out that the Nvidia driver crashed. It seemed the longest I let this go without plugging back in, the worst the symptoms would get until the computer was almost completely unresponsive.

Originally I believed the &#8220;unplugging&#8221; action that caused it was unplugging the AC power cord. That seemed to make sense to me because I figured that going to battery power might cause some weird performance issues. Google revealed people with the same problem as me, who got [100% CPU usage after unplugging power](http://www.aintageek.com/solution-to-windows-7-100-cpu-usage-after-unplugging-ac-power.htm). However, their solution didn&#8217;t help &#8212; I was already using High Performance mode and all of the processor settings were set to maximum even when on battery power.

However, when I started to troubleshoot, I unplugged each device one by one. First the mouse. That didn&#8217;t cause it. Then the power. Oh, wait&#8230; that wasn&#8217;t the cause after all. And sure enough, when I unplugged the Ethernet, the 100% CPU usage would begin. I plugged the power and mouse back in and the computer was still sluggish. Within 2 seconds of reconnecting the Ethernet, the problem disappeared and my problem was back to normal.

So, how exactly do you solve an issue where unplugging an Ethernet cable leads to 100% cpu usage? I should also mention this was ethernet specific, and didn&#8217;t involve lack of Internet, since I had wireless enabled this entire time and could browse the Internet (albeit slowly due to the sluggishness) while the ethernet was unplugged. Well, eventually I found a thread about a somewhat similar problem, where the user had [high latency corresponding with network usage](http://www.sevenforums.com/network-sharing/52935-network-usage-causes-high-dpc-latency-3.html).

**Solution:**

The linked forum thread actually has many solutions in it. I tried all of them and none of them actually worked for me. I finally decided to just use the workaround posted in the thread, which is to simply disable my ethernet adapter (in Network Adapters window right-click on it, select &#8220;Disable&#8221; ). This solved the problem completely, and it persists across restarts. I should mention that the tools [xperf](http://msdn.microsoft.com/en-us/performance/cc825801) and [LatencyMon](http://www.resplendence.com/latencymon) were invaluable in finding this forum thread, because I never would have known the problem was caused by &#8220;ndis.sys&#8221; without those two programs.

I still don&#8217;t see why this caused the above symptoms. There must be some bug in Windows 7 where certain laptops have this problem. But just like so many [curiosities](http://en.wikipedia.org/wiki/Problem_of_evil), this one probably has no rational explanation.