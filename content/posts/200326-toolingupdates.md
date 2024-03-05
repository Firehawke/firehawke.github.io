---
title: "Tooling updates"
date: 2020-03-26T22:17:31-07:00
draft: true
toc: false
images:
tags:
  - Hugo
  - WSL
  - SSH
  - VSCode
  - BoxStarter
---

I hit an interesting problem with Hugo this morning. Something about the previous post's generated files could not be contained on a NTFS filesystem any longer. I didn't feel like digging into exactly why this was the case; instead it gave me incentive to sit down and update my OS rebuild scripts and get more of my setup into private Git repositories.

Admittedly this may sound like a non-sequitur at first, but there's a strange sort of logic behind everything. My first thought was "Okay, if I can't do it from Windows, I'll use WSL to do the work."

From there, I realized that I was going to need to install Hugo, and that in turn was going to need me to install Go. I decided that I was going to need a script to handle this just in case the WSL distro ever gets mangled beyond repair. I have one using BoxStarter on the Windows side of things, but I didn't have one on Linux yet-- so that was the first steps, build a script that would automate as much of the process as possible.

After that, I decided I needed to get a bit more of my private tooling backed up into a Git repository. *It really ends up being a recursive sort of task; the more you get done, the more you realize you need to do.*

While googling some of the information I needed to know, I found a way to use some of the stock GNU tools in the Windows MAME msys2 install to parse Github's APIs and download (and install) the latest versions of certain tools I keep in my utilities folder (e.g. [YouTube-DL](https://github.com/ytdl-org/youtube-dl), [WSL SSH Agent](https://github.com/rupor-github/wsl-ssh-agent)) so I ended up writing a script for that too. In retrospect, Chocolatey will probably have 90+% of the packages I'd need that script for, but it'll still be useful for the occasional outlier.

Speaking of [WSL SSH Agent](https://github.com/rupor-github/wsl-ssh-agent), that's also a pretty major find as well. This tool sets up a socket redirection to let WSL access the ssh-agent on the Windows side of the fence. In short, this will fix some of the most irritating issues that VSCode has with SSH-based Git repos in a WSL environment.

There *IS* one security drawback: If I allowed anyone else to SSH to my WSL install, they could find where the socket file is and get access to my SSH keys that way. Since I'm not allowing SSH to the WSL install, that's not a problem for me.

All in all, a pretty productive evening. I think I just lost about six hours without even realizing that much time had passed.

{{< sig >}}