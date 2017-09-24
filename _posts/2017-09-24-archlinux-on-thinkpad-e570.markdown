---
layout: post
title: ArchLinux on Lenovo ThinkPad E570
---

I've been running ArchLinux on my new Lenovo ThinkPad E570 notebook for quite some time now. All things considered, it has been a very pleasant experience so far. Let me highlight some of the attractive features as well as point out some pitfalls. Let's begin with the latter:

# Intermittent WiFi connection

My laptop uses the Qualcomm Atheros QCA6174 Wireless Network Adapter which is a common piece of hardware. You can see it in other laptop lines such as Dell XPS 13 and 15, Acer Aspire V15 and V17 Nitro, Asus AsusPro series, ROG series etc. In August 2017 my WiFi connection became unstable and it was not easy to troubleshoot. After a trial-and-error process (try a different laptop, try a wired connection, try a different router) the problem was localized to the E570 laptop. The `dmesg | grep ath10k` was also showing a suspicious `Unknown eventid: 90118` which finally allowed me to [find a solution][1]. In short, `linux-firmware` is at the moment shipping a buggy `/lib/firmware/ath10k/QCA6174/hw3.0/firmware-6.bin`. You could rename that file and reboot which will force a previous version of the firmware to be used instead:

```
$ sudo mv /usr/lib/firmware/ath10k/QCA6174/hw3.0/firmware-6.bin /usr/lib/firmware/ath10k/QCA6174/hw3.0/firmware-6.bin.bak
$ sudo reboot
```

# Short List of Advantages

My opinions are based on over 6 months of active use.

1. Fantastic keyboard
1. Impressive screen
1. High assembly quality

# Requires Additional Configuration

Some of the problems below would probably fix themselves if you use Gnome (or KDE, or some other feature-rich Desktop Environment). However, I am running a simple i3 Window Manager, so a lot of things require additional attention:

1. Brightness keys
1. Not a round-robin keyboard layout switch

[1]: https://superproxy.crushus.com/bbs.archlinux.org/viewtopic.php?pid=1728715#p1728715
