---
author: rob
categories:
- General Stuff
date: "2006-03-01T19:30:09Z"
guid: http://eatyourexam.com/?p=20
id: 20
title: Midpoints to Vertices Program
url: /?p=20
---
In Geometry today, we &#8220;learned&#8221; how to take the three midpoints of a triangle and then find the unknown vertices of that triangle. The process is rather basic Algebra, but extremely tedious and long. This is the perfect application for a program. I whipped up a Perl script in about forty minutes (most of that was looking up Perl commands, as I don&#8217;t use it as often as C++ and forgot a lot of the basics), and it worked beautifully. The reason I did it in Perl is this: Perl, by use of the wonderful thing called CGI, can be run on a website. That is, any Perl script can be made into a website of the same functionality with minimal effort. My goal in making this program was to make it accessible on this site, and it now is thanks to CGI!

For those of you who are impatient, click [here](http://eatyourexam.com/my-sites/midpoints.htm "Midpoints to Vertices Program") to get to the program. While it obviously facilitates this stupid homework assignment, it represents much more than that. By successfully creating this program I now know how to do CGI to at least convert the textual output of a Perl program to an HTML page. Therefore, any program I can write in Perl I can put on the web. That is a very cool concept for me, and I expect to be using Perl much more in the near future because of that. Not to mention, my web server supports CGI so I might as well get my money&#8217;s worth 😉

One side note. Today marks the beginning of March. If you look to the side bar, you will notice that there are currently no more top commentators. It resets every month. I can change that, but I don&#8217;t think it is necessary. Resetting every month will hopefully influence people to comment every month&#8230;