---
title: "Resurfacing with projects"
date: 2020-05-09T18:11:15-07:00
draft: false
toc: false
images:
tags:
  - Surface
  - MAME
  - Apple II
---

I'm currently in the middle of a major chunk of MAME documentation; one could successfully argue that I'm resurfacing it-- in more than one way. The primary goal is to work out some less than user-friendly parts of the commandline parameter section of the documentation. That is proving to be about as time-consuming as I had expected.

When I took on the job of redoing the docs in 2014, many sections of the docs were upwards of 10 years old. I've been working on it ever since, with about a year's break until now. I've also come to realize that some pieces of documentation are entirely missing, lost in various transitions over the years (e.g. SDLMAME into MAME, MESS into MAME, etc). Finding information on these undocumented sections is proving to be the biggest time sink; most of the documentation is already ready to submit, but these last few pieces are the major hold-up.

The biggest problem of all is the OpenGL shader plugin system. There are several components to this particular headache.

1. It was implemented by someone outside of MAMEdev and as far as I can tell never updated by them. There was one MAMEdev update that I'm aware of, but that was years ago.
2. The docs that were provided were primarily aimed at developers looking to generate plugins. This leads into...
3. The system included in MAME itself only included two or three very basic plugins. The most popular plugins were provided outside MAME in packages, which leads to...
4. The most popular plugins are hard to find and download; many may not even exist at this point. Even if I could find them, I couldn't include them in the MAME package without getting licensing squared away on these plugins.

I think the best thing I can do at this point is to document what I can out of what's here in the mainline MAME package, then port the old programmer-specific documentation over to the MAME developer wiki.

So, back to the original point-- I made an allusion to resurfacing. I managed to get my hands on a used (but nearly perfect condition) Surface Pro 4 about two weeks ago. I've been using it for a lot of my editing since it's recent enough to run Windows 10 (and the necessary mitigations for Intel's recent design flaws) just fine. I've tried pushing the hardware a bit for fun and found it plays a number of games reasonably well-- it'll be great to be able to take the [Ephinea PSO server](ephinea.pioneer2.net/) with me when I'm on a doctor visit as I'm usually in the office for at least 2-3 hours of delay time between sitting in the office after arriving and sitting there waiting for transport home. My health and medications make it impossible for me to drive, so I'm heavily reliant on medical transport.

Oh, and the Surface plays MAME stuff reasonably well. I need to find some way to tweak MAME to deal with the autorotation problem, though. I seem to recall there's a way to specify settings for that in a manifest file. I'll need to dig into that.

As for Apple II, I'm slightly behind but it's not a noticeable thing. It'll take me less than 30 minutes to get caught up. In fact, I'm probably going to switch branches and get that done tonight. It'll be a good distraction from the documentation headaches.

{{< sig >}}