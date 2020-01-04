---
author: rob
categories:
- Gaming
date: "2007-04-05T15:59:21Z"
guid: http://eatyourexam.com/?p=89
id: 89
title: Nintendo DS Save Converter
url: /?p=89
---
I received my awesome black-colored DS Lite in the mail on Monday and I’ve been playing it ever since. I’ve been experimenting with various programming tasks for creating programs that run on the DS itself — let’s just say that I’m not doing too well. My biggest plan is to make some way that will allow me to cheat on ROMs. The combination of my flash cartridge with ROMs makes it impossible to do what I want with any pre-existing methods. Hopefully I’ll make progress soon, but as of now things are looking bleak; I barely understand how to access the DS’s memory, let alone how to hook certain functions and modify memory dynamically at runtime (which I will need to do to be able to cheat in the games).

That said, I have accomplished at least one thing. It turns out that most of the save game files available on internet message boards and sites such as [GameFAQs](http://gamefaqs.com) are in the format created by an Action Replay DS (they are .duc files). The problem is that my flash cartridge does not support these kind of saves, and instead uses a 4-mbit raw SAV file format. In order to combat this, I made a program in Visual Basic that converts between the two formats. Also, I made it so you can also convert to 2mbit raw SAV files, which is what most flash cartridges other than mine use.

You can see the entry for it on the [My Programs](http://eatyourexam.com/?page_id=6) page of this site, or you can simply click [here](http://eatyourexam.com/my-files/progs/NDS_AR_Save_Conv.exe "NDS Action Replay Save Converter EXE Download") to download it directly. I tested it with Windows XP and Vista, but it should be compatible with any Windows as long as you have the runtime file available [here](http://eatyourexam.com/my-files/progs/msvbvm60.zip "Microsoft VB 6 Runtime DLL (ZIP)").

Enjoy. If you have any trouble using it or have a feature request, let me know in the comments section.