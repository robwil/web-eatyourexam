---
author: rob
categories:
- General Stuff
date: "2006-07-31T15:34:53Z"
guid: http://eatyourexam.com/?p=57
id: 57
title: 'del.icio.us (Tiny): Firefox Extension'
url: /?p=57
---
One of the best things about Firefox is its extensions interface. You can add functionality and features with a few clicks of the mouse. There are hundreds of these extensions available at Mozilla&#8217;s official site [here](https://addons.mozilla.org/). (Hmm.. what a coincidence that the Featured Add-on for today is the del.icio.us Extension that I&#8217;m going to talk about in the rest of this brief article) There are many other sites online with bigger repositories, but I just stick with the officially uploaded ones. The second best thing about Firefox is Themes, which are skins you can apply to your browser to make it look different. It will have different Forward, Back, Stop, Refresh, Home, etc. buttons and more. You can get themes from Mozilla&#8217;s site as well.

The problem is that sometimes the Themes and Extensions don&#8217;t work too well together. Extension developers think you will use the default theme, and so the buttons they use on the toolbar may not have good enough transparency masking to look good with a different background (adding a black theme when you have tons of extensions will show you tons of artifacts around the edges of icons). Another problem is that the icons may be too large if you chose to use a minimal theme (like me).

I recently started using the theme called [del.icio.us extension](http://del.icio.us/help/firefox/extension) has toolbar icons that are way too big. It looks completely stupid to have these giant del.icio.us icons next to tiny browser buttons. Also, it defeats the purpose of using smaller icons since the toolbar itself will be the same size as the default because of the no-good large icons of the del.icio.us extention.

So, what on earth did I do to fix this annoying problem? I tapped into the hidden potential of Firefox&#8217;s extension system&#8230; the ability to modify them to do what you want. In the case of this extension, I didn&#8217;t have to modify anything other than a CSS file, then rename some images. Regardless, my little hack worked like a charm.

I figured I would repack it into an XPI file and share with others that may need the same functionality. You can click [here](http://eatyourexam.com/my-files/delicious.xpi) to download it. Firefox will ask you what to do with the file. Just download it to the desktop and then, while inside Firefox, go to File->Open File and double-click the file. It works with Firefox version 1.0 &#8211; 1.5.0.x. Enjoy 😉

By the way, just for those of you who care about such things, the XPI files used by Firefox extensions are just ZIP archives with a different extension. You can unzip it with WinZIP or anything similar, or using the CLI with the &#8220;unzip&#8221; command.

To give you an idea of just how small this mod makes the icons, look at the following image of my Firefox toolbar. This is the actual size of everything:

![My Firefox Toolbar](http://eatyourexam.com/my-images/toolbar.jpg "My Firefox Toolbar")