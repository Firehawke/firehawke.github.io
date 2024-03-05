---
title: "Calculated Risks"
date: 2020-04-19T16:56:06-07:00
draft: false
toc: false
images:
tags:
  - Windows 10
  - WSL2
  - Apple II
  - MAME
---

I'm about to do something slightly risky and install the "release preview" build of Windows 10 V2004. It's a very calculated risk, though-- I still have my ~9-year-old laptop running Debian Linux if things go completely haywire. Why am I taking this particular risk? I'm pretty reliant on WSL for a lot of what I do these days; most of my softlist flow uses scripting for Bash with substantial additional use of wget, lftp, and ROMVault.

Performance on WSL1 has been a sore point of the process. In particular, filesystem access speeds on WSL1 are terrible-- but that's equally the fault of WSL and the absolutely undeniable fact that Windows 10 has abysmal read/write speeds in general. WSL2 allows me to use a native Linux filesystem (in this case, it most certainly will end up being EXT4) and that will help the chugging issue.

I hope I don't have to reinstall Windows after this is over with, but if I do it won't be a completely horrible situation at least.

We'll see how well this comes out.

{{< sig >}}