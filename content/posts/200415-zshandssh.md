---
title: "Zsh and SSH: UTF-8 gone haywire"
date: 2020-04-15T18:58:54-07:00
draft: false
toc: false
images:
tags:
  - Zsh
  - SSH
  - UTF-8
  - Unicode
  - DHCP
  - Pi-hole
---

Well, just got done debugging a very weird issue I was having with UTF-8 encoding. It was working fine locally (Windows 10) from both PowerShell and the WSL Debian distro I'm using, but the UTF-8 would stop working correctly as soon as I connected to my [oDroid C2](https://wiki.odroid.com/odroid-c2/odroid-c2) running [Armbian](https://www.armbian.com/). This would manifest itself in my prompt no longer being able to show UTF-8 characters and the inability for cursor placement to work correctly.

I spent about two hours digging into this. At first I thought it was a problem on the Windows side since UTF-8 support in Windows Terminal is still a pretty new thing. Nope, everything was working just fine. That's about the point I started wondering if it wasn't something specific to the Armbian configuration.

Turns out that was exactly what it was: the distro shipped with the line "LC_ALL = C" in the '/etc/environment' file which *should not have been there*!

Quoting the [Debian wiki](https://wiki.debian.org/Locale):
```
Warning!

Using LC_ALL is strongly discouraged as it overrides everything. Please use it only when testing and never set it in a startup file.
```

Removing that line fixed the issue immediately.

Of course I should also briefly comment on why I was SSHing into the machine in the first place, right? I'm using the C2 as a [Pi-hole](https://pi-hole.net/) server.

A few weeks ago, I had been fighting a particularly annoying problem with my Netgear R8000 router. It doesn't like using a /16 on 192.168.0.0, but only chokes on a reboot. It will work perfectly fine until you reboot, and at that point it breaks down and goes back to default settings with an error message that it's conflicting with something on the ISP side. There certainly shouldn't be anything conflicting with the 192.168.0.1 address it uses! The router isn't acting as DHCP, either; that's all on the oDroid C2 along with Pi-hole setup. I should consider migrating the ISC DHCPD configuration over to the native Pi-hole DNSmasq-based system at some point in the future.

Well, I decided to give in and approach it completely differently. I moved everything to the 10.0.0.0 range today, and that's when I noticed the prompting issues.

{{< sig >}}