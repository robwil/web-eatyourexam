---
author: rob
categories:
- Howto's
date: "2006-02-05T12:40:35Z"
guid: http://eatyourexam.com/?p=9
id: 9
title: 'iPod Video Conversion Part I: Basic Conversion'
url: /?p=9
---
There are many different programs and methods available to convert videos to iPod format, but I use a program called Videora iPod Converter because it is free and converts files quickly. Get the program [here](http://www.videora.com/en-us/Converter/iPod/ "Videora iPod Converter Homepage"), and then install it. During installation, uncheck the box that says “Launch at Startup”, but keep “AViSynth” checked. Launching it at startup is not necessary and will just slow down your computer.

After it is installed, run the program. In this main screen, look in the left side bar. Press Convert. That is where you will do most of the work. Press the button that says “Transcode New Video”. Browse to the location where your video file is stored and open it. The file name will now appear in the Title box under “New Transcoding Job”.

The last thing you need to concern yourself with is the part that will require the most thought. You need to choose the Quality Profile. You need to take three things into consideration when you pick a profile:

  1. The file size of the video.
  2. The quality of the output video.
  3. The time it takes to convert the video.

It is balancing these three things that gets somewhat difficult. If you make the best possible quality video file, the file size for a 2 hour movie will be about 1500MB. Also, the more quality you have the longer it will take to convert the file. So, I tend to convert files with medium settings, since that will give you a nice balance between size and quality. I prefer MPEG-4 over H264, since it is generally a smaller file with better quality, but it really depends on what kind of movie you are converting.

In order to figure out what Profile to use, go back over to the left side bar and click Setup. On the top of the new screen will be four tabs. Choose Profile Picker. In the dropdown box next to One-Click Profile, there are MANY options available , so just look through a bunch of them until you find one that looks good. The key things to pay attention to is the quality of video and audio at the top, and then the file size near the bottom of the screen. Depending on how many movies you intend to carry on your iPod, you should definitely not go for the best. To get the best results, experiment. I use MPEG-4/320×240/512kbps Stereo/96kbps as my main profile for most files, since it perfectly balances quality with file size. A 2-hour movie will only be around 580MB.

I only use the best profiles when I’m converting a movie I know I will keep for a long time and watch many times, though I really can’t see a quality difference between the medium and best profiles.

Once you have selected the profile you want, click on Convert again. Choose your profile from the “Quality Profile” dropdown box. You are now ready to convert the video. Now press the Start button, and your video will begin to be converted. This part is where Videora really shines. It is pretty fast. It takes about half the amount of time as the source file. So, if you are converting a two hour movie, it will take about an hour. TV shows which are usually 43 minutes without commercials take around 25 minutes. Compare this to Quicktime Pro, the program that Apple wants you to use (and which costs $29.95), where it takes about an hour and a half to convert a 20 minute file!

Anyway, once your video is done transcoding, it will say “Transcoding Complete”. The converted file will be located in C:/Program Files/Videora iPod Converter/Videos. After you go there the first time, you can right-click on the Videos folder, go to Send To, and then “Desktop – Create Shortcut” to make a desktop shortcut for easy subsequent access. Once you have the Videos folder open, open up iTunes. Once it comes up, just drag the video you converted from the open folder to the Library item on the side bar. Next, open up the Videos item, and you should see the video you converted listed. If you want, you can right-click on the video and go to Get Info and change the name of the video, artist, etc. just as if it was a song. Anyway, now you just need to plug in your iPod to copy over the file, and it should be ready to watch on the iPod’s screen.

There are many more programs available now since the iPod Video has been out for a few months that I have not yet tried, but I see no reason to switch from Videora iPod Converter. It converts quickly, it’s free, and it gives you plenty of options. A widescreen movie converted using the medium settings above looks pretty good on a 50″ television, and looks incredible on the iPod’s 2.5″ screen.

One last thing I would like to note is widescreen video. If the video you are converting is widescreen, and not a square, then no matter what setting you use in the program it will look stretched. It isn’t that bad, but it could be annoying if you want the best possible quality from your files. In order to make a widescreen video that will play on your iPod with no stretching, follow the below steps.

Open up Videora iPod Converter and go to Setup. Then go to the Profiles tab (not Profile Picker). In the screen that comes up, select a profile that you found works good for you from the top dropdown box that says “Existing Quality Profiles”. If you don’t know what to choose, just use my recommended one above. Press the “New Profile” button. After this, first change the “Profile Name” to something like “Widescreen Video”. You could also append the 512kbps, etc. if you plan on making more than one Widescreen profile. Now, the only thing you need to change is “Resolution”. Type 368×208 into the box. Now press Apply. This will save the profile and you can now use it within the Convert window to make non-stretched iPod videos. This is the ideal resolution setting to convert DVD-ripped videos to iPod.