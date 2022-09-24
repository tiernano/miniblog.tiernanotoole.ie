---
title: Day 101 of 100daysofhomelab
date: 2022-09-23T23:00:00+00:00
tags: ["homelab", "100daysofhomelab"]
---
Day 102 of #100daysofhomelab and still fighting with my Cloudflare Workers stuff.

* I though i had added caching to it, but it looks like i broke something. Its writing the result to cache, but not able to read it properly... 
* on the more homelab side of things, just gone though some boxes and checked their update status. 
* want to move all my old docker stuff from my docker vm, aptly named `docker` to my new `new-docker` box. or even build a third one. Ideally, chance the names to `docker-01` and `docker-02`. 
* Still wanting to move GodBoxV3 from Windows Server 2022 over to ProxMox. It currently has 2x20 Core Xeon Gold processors, 256GB RAM, 2x512GB NVMe drives in RAID for boot, 5 more 512Gb NVMe's in RAID for fast storage, 8x8TB HDDs for bulk storage and 2x960GB SSDs for other storage... It also has a Quadro P2000 Graphics card in there. 
* If i get it moved to ProxMox, i could set up TrueNAS as a VM with most of the disks, plus then build a Plex Server with the P2000. More work required.
