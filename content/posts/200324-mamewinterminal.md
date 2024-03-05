---
title: "MAME and Windows Terminal"
date: 2020-03-24T22:20:58-07:00
draft: false
toc: false
images: 
tags:
  - MAME
  - Windows Terminal
---

I've become a pretty big fan of the new [Windows Terminal](https://github.com/microsoft/terminal/) in the last year or so. It's more responsive than the [ConEmu](https://conemu.github.io/) that I was using previously, and the integration with WSL is pretty nice for my workflow. That said, it took a little work getting it just right with the MAMEdev-provided [msys2](https://www.mamedev.org/tools/) package.

So I'm going to share my configuration information so you can save a little time in getting Windows Terminal set just right.

Start Windows Terminal and bring up the Settings page. This will open the `settings.json` file in your default editor. You can add an entry like the following:

```json
		{
			"name": "Dev environment",
			"startingDirectory": "c:\\msys64\\src",
			"commandline": "cmd /k ..\\win32\\env.bat",
			"fontFace": "Cascadia Code",
			"fontSize": 14,
			"hidden": false,
			"backgroundImage": "c:\\msys64\\MAMELogoTM.jpg",
			"backgroundImageOpacity": 0.2,
			"backgroundImageStretchMode" : "uniform",
			"backgroundImageAlignment" : "center",
			"colorScheme" : "FH-VGA"
		},
```

The name chooses what it will show up on the menu of selectable consoles as. The starting directory and commandline assume that you've installed the MAMEdev msys2 package in the default location of `c:\msys64`. I've installed the [Cascadia Code](https://github.com/microsoft/cascadia-code) font and wish to use that in the terminal. I've added a dim [background image](/images/03-2020/MAMELogoTM.jpg) to my terminal, which is conveniently located at `c:\msys64\MAMELogoTM.jpg` on my machine, and I want it centered and looking unstretched.

Lastly, I'm using a custom color set that mimics the 16 standard VGA colors of the 1990s. You may wish to leave that line out, of course.

The end result looks a lot like this:

![image](/images/03-2020/mamedevterminal.png)

{{< sig >}}