---
title: "PowerShell and Zsh: Part 2"
date: 2020-03-30T16:00:11-07:00
draft: true
toc: false
images:
tags:
  - MAME
  - PowerShell
  - Zsh
  - Posh-Git
  - Powerlevel9K
---

As I'd expected, PowerShell is a pretty major departure from pretty much any other scripting system I've ever learned. I seem to have managed to also hit a pretty nasty bug that's been known about for a very long time-- PowerShell seems to completely choke when hitting filenames with brackets like `[this].txt`-- even escaping the brackets doesn't work as it should and processing chokes. I ended up having to do OS-specific workarounds for moving files in a script (call `CMD.EXE /C "move"` on Windows, directly call `mv` on Linux/MacOS) to avoid hitting that brick wall head-first.

Can't say I'm entirely thrilled with that, but at least on Windows PowerShell is absolutely the future going forward. It doesn't hurt that I added [posh-git](https://github.com/dahlbyk/posh-git) to my install, making it much easier to keep track of what I'm doing to any of my Windows-side projects. [Powerlevel9K](https://github.com/Powerlevel9k/powerlevel9k) does the same thing in Zsh for Linux.

I have pretty serious problems with my short term memory. It's safe to say I was somewhat absent-minded when I was younger, but Fibromyalgia has utterly wrecked my memory. I can lose my phone after setting it down for 30 seconds, as one example. I try my best to do workarounds for my memory issues by setting routines like putting my phone and wallet in the exact same place if possible, making sure my black phone isn't sitting directly on my black desk (as opposed to a white plastic space on the left side of my desk), and so forth.

This also applies to work on the computer itself. Anything that I can do on the computer that will let me augment my memory with the computer's memory is a good thing. I keep large quantities of notes on my computers, all synchronized to private cloud storage so I can't easily lose those notes.

What I'm predicting is going to happen with PowerShell in particular is that I'm going to mostly get the feel for it after using it for a substantial amount of time, but like every other language I won't be able to retain exact syntax and I'll be constantly referencing my own scripts and online texts to remember exactly how to put things together. It's frustrating that I can't actually memorize things like that, but no amount of medication seems to be able to restore me to my former self. I can only be glad that I retain the fundamental theories behind programming (and make no mistake, scripting IS programming) enough that I can still muddle through by referencing books for exact syntax on what I want to do.

I'm also currently fighting a fairly major ISP issue again. There's something very odd going on, and I'm predicting it's probably external wiring-related. My downstream looks mostly fine, but it does wobble quite a bit in the range of 130-170 Mbps. The upstream... that's wobbling extensively in the range of 0.30 Mbps (which is what pushed me to call my ISP to complain!) to the normal 20-30 Mbps. There's no pattern to how/when it gets better or worse, either.

Of course none of this is even remotely surprising. The local maintenance supervisor, Jason, has told me in the past that they know they have a node issue in this neighborhood but they can't find the piece of hardware that's malfunctioning. I've had reoccurring issues with my connectivity since I moved into this location seven years ago, and it's changed my satisfaction with this ISP from "They're great!" down to "Well, if you have a neighborhood that's getting maintained they're pretty good, but otherwise you're screwed."

Well, guess it's time to get back to work. I should see what new Apple disks are out so I can get them added to MAME.

{{< sig >}}