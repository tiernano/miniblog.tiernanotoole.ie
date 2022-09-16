---
title: Day 94 of 100DaysOfHomeLab
date: 2022-09-16T21:50:00+00:00
tags: ["homelab", "100daysofhomelab"]
---
Day 94 of 100DaysOfHomeLab and I have been playing with OSPF, GRE Tunnels, Mikrotik, Bird and ECMP.

* I got 2 [GRE](https://en.wikipedia.org/wiki/Generic_Routing_Encapsulation) tunnels setup between the MikroTik box and my DEC-IX box (Debian running Bird).
* [OSPF](https://en.wikipedia.org/wiki/Open_Shortest_Path_First) running and announcing stuff over those 2 links, plus the original Wireguard Link.
* [ECMP](https://en.wikipedia.org/wiki/Equal-cost_multi-path_routing) enabled over all 3 links!
* IPv4 traffic seems to be sent between the 3 links! 
* IPv6 traffic still only going over the single Wireguard link...

I am reading up on OSPF v3 (v2 is for IPv4 traffic) and trying to figure out how to get it running. So far, no luck... Getting so close to it though.

Whats the end game? both WAN links connected to all 3 of my upstream servers ([Vultr](https://www.vultr.com/?ref=6925432), [VMHaus](https://www.vmhaus.com/) and [DEC-IX](https://www.de-cix.net/) box) allowing more stable connections and more bandwidth (hopefully...)

Next week I am OOHL (Out Of Home Lab...) but will still try do a bit of work. Fingers crossed!