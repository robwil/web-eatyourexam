---
author: rob
categories:
- Tech
date: "2007-05-31T20:53:53Z"
guid: http://eatyourexam.com/?p=92
id: 92
title: My Mini-ITX Project (Pics now up!)
url: /?p=92
---
<p align="center">
  <img src="http://eatyourexam.com/photos/albums/uploads/mini_server/normal_009.jpg" alt="My Mini Server" />
</p>

UPDATE (05-31-07): I finally got the pictures up for the Mini-ITX server. Check them out [here](http://eatyourexam.com/photos/thumbnails.php?album=6). If you are interested in the components behind it, read the original post below.

——————————————————————————————-

As you may or may not be aware, there is a certain motherboard specification called Mini-ITX. It was pushed to the market mainly by VIA, though there are many offerings nowadays. Essentially, it follows the ATX standard, but condenses all of the motherboard components down to a 6.75″x6.75″ board. Also, the motherboard has sound, network, video, and CPU all built into it. Even better, most of them contain no fans, and instead use heatsinks to cool the CPU and chipsets… this passive cooling cuts on power usage and also makes the system 100% silent. All that needs to be added to such a motherboard to make a full computer is a form of persistent storage (hard drive, etc.), RAM, and power supply. Optionally, a disk drive and other accessories can be added. All of this uses very little power (think 30-50W, as opposed to modern gaming computers that use around 550W) and runs relatively cool.

When I started my project, I was aiming at making a headless (meaning it has no monitor, keyboard, and mouse, and is instead controlled from other computers over the network using technologies such as SSH and/or VNC) Linux server. I chose Linux for a lot of reasons, but mainly because it can support low-end systems and is highly customizable (and thus can be a large or small as I want it to be). That said, I went and purchased the components on eBay. For the motherboard itself, I picked what was the original Mini-ITX board offering from VIA, the EPIA 5000. It contains a 533mhz C3 processor, plus built-in sound/video/network. I already had a piece of 256MB PC100 Ram, so all I needed in addition to the board was a hard drive and power supply. For the hard drive I chose to go with a Compact Flash card (and thus needed a CF -> IDE adapter to connect it to the motherboard as if it were a real hard drive), and got a 512MB one. It has turned out to be enough room, but things are definitely tight. Finally, for the power supply I went with the Morex PW-60, which as you may be able to tell from the name, is a 60W offering. The power supply itself is about half the size of a modern AGP video card, and it is the only part of the system that makes any noise (it doesn’t have any fans, but it has a slight “hum”).

Once all the pieces that I had ordered arrived, it was as simply as popping in the RAM, connecting the CF card via my adapter, and then plugging the power supply into the motherboard and a power outlet. I temporarily connected a CD drive to install the Linux OS (I chose Damn Small Linux because of my tiny 512MB hard drive limitation and because it is based on my favorite distro: Debian) and also temporarily used my main PC’s monitor, keyboard, and mouse. I installed the OS, then made sure SSH was working correctly. Once that was done, I disconnected all of the accessories and removed the CD drive. I then SSH’d into it from my main computer and went to work.

I have installed a variety of things onto it in the past week. For starters, I installed HoTTProxy, a proxy server that can be utilized by cell phones. It is the only service I know of that gears itself specifically to cell phones, and is ridiculously easy to setup (just create a user, run the program and point your phone to it). Not to mention the fact that it keeps a cache which speeds everything up. This worked with minimal effort, as I used Damn Small Linux’s package system (myDSL) to install the required Perl.

Next I aimed to get VNC working on it. Again, this was a breeze with the myDSL system. I had to make some hacks to get the vncserver to start on bootup (the package didn’t create a nice /etc/init.d/vncserver script, so I manually added a line calling the server process from the local run-at-boot script that DSL utilizes). One additional thing I had to mess around with was getting a static IP address (necessary for router port forwarding so that I could SSH and VNC in from the Internet, i.e. from school/work). The usual Debian way just didn’t work with DSL, so I again solved it by putting the manual “ifconfig” and “route add gw” entries into the local run-at-boot script.

My final goal was getting a web server with PHP support installed. I chose to use lighttpd mainly because of its low memory footprint and its speed. It includes FastCGI, which interfaces very well with PHP4. Anyway, using the myDSL packages for PHP did not work because they were not compiled with FastCGI support. So, I had to resort to the old “wget, tar xvzf, cd dir, ./configure, make, sudo make install” method, which I am well-accustomed to from my old Linux From Scratch days. Nonetheless, I eventually got the two to work together, and it is now running. I also added eAccelerator, the PHP caching tool that caches opcodes among other things, hoping that it may speed up whatever application I eventually deploy on the web server.

With all the software taken care of, I now look at my semi-completed Mini-ITX Server. I face one last hurdle… that of a case. I purposely chose not to buy a case, both for monetary and DIYish reasons. So, hopefully some time in the next few weeks I will come up with a good idea for how to house the components. A 7.5″x7.5″x3.5″ container of some sort would fit everything and then some. I don’t, however, want to simply use one of the oft-used cop-outs like a cardboard box or a cigar case. I want something original. I’m currently looking into a hermit crab cage or small fish aquarium, but they’re a little too pre-made for me. We’ll see what I come up with.

In the mean time, I am going to be slowly adding pictures of the currently caseless build to my Coppermine photo gallery that has been long neglected, which can be reached [here](http://eatyourexam.com/photos). I am not, however, making any promises on when those will be up.