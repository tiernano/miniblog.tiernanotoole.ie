---
title: "Day 123 100daysofhomelab"
date: 2022-10-15T21:12:02+01:00
tags: ["100daysofhomelab","homelab"]
---
Day 123 of #100daysofhomelab and i *think* I finally sorted out Bird 2.0!

* It looks like Bird 2.0 is up and running, announcing stuff correctly, and the like. More testing required, but happy days!
* I also started announcing my new V4 and V6 space though [VMHaus](https://vmhuas.com), using Bird 2.0. Now to do the same with [Vultr](https://www.vultr.com/?ref=6925432) and my DEC-IX box.
* Have been having issues with DNS for the last few days. I think its Active Directory Related. My PiHole is set to use the AD boxes as their next hop, then AD is using [NextDNS](https://nextdns.io/?from=3dvjhcum) as its upstream... I updated PiHole to now use the AD DNS only for [internal DNS queries](https://www.vikash.nl/use-pi-hole-with-microsoft-active-directory/) and things are starting to get a bit faster... Maybe my AD boxes are under powered, cause I have run Windows DNS for a long time before and never had issues with perf for DNS... Weird...

More re-numbering for tomorrow and hopefully upgrading the Vultr box to Bird 2.0. The one in DEC-IX will be a larger move... More peering connections to fix... We will see how things go!
