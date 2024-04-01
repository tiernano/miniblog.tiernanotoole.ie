---
title: day 104 of 100daysofhomelab
date: 2022-09-26T20:10:06+01:00
tags: ["homelab", "100daysofhomelab"]
---
Day 104 of #100daysofhomelab and not major going on. Back in $dayjob, so busy catching up with that. Some links, news and updates below:

* Found a [VSCode](https://code.visualstudio.com) plugin for adding timestamps to files called [VSCode InsertDateString](https://github.com/jsynowiec/vscode-insertdatestring). makes adding the time to markdown files easier.
* Cloudflare have announced a [new Zero Trust SIM card](https://blog.cloudflare.com/the-first-zero-trust-sim/). This could be very cool! For me, I am thinking a basic data only SIM would work in the tracker in my car (low data usage). A higher data usage option would be the 4G router in the boot/trunk of the car giving Wifi Access to my Dashcam (you can read more about that [here](https://www.tiernanotoole.ie/2022/02/25/running-a-raspberry-pi-in-a-car-and-backing-up-dashcam-footage.html)). I wonder what would happen with phone calls and text messages though? Is it going to be data only?
* Still looking at the [hugo migrations page](https://gohugo.io/tools/migrations/) for moving from Wordpress over to Hugo for the main site...
* And since this is a homelab post, just a note on the whole [Proxmox auth with Azure AD](https://miniblog.tiernanotoole.ie/posts/proxmox-azure-ad-auth/): You cant open a terminal when you use that feature... There is probably a setting i am missing, but you will still need to login as root to open a terminal...
* Also, [apt-cacher-ng](https://www.unix-ag.uni-kl.de/~bloch/acng/) is working very well. Updated all 3 proxmox boxes today. only used about a third of the bandwidth to do updates!
