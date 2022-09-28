---
title: Day 106 of 100daysofhomelab
date: 2022-09-28T20:25:44+01:00
tags: ["homelab", "100daysofhomelab"]
---
Day 105 of #100daysofhomelab and I am still trying to get my [VMHaus](https://www.vmhaus.com/) Box running Bird 2.0. Its running, just not configured right. And some news updates too.

* managed to get [Bird 2.0](https://bird.network.cz/) and [Mikrotik](https://mikrotik.com/) talking to each other, but the Mikrotik is announcing only V4 routes to Bird. No V6. And Bird is not announcing ANYTHING to mikrotik... 
* upgraded all my Ubuntu and Debian boxes. Need to automate that with [Ansible](https://www.ansible.com/) at some stage... 
* Video series from Mikrotik about running Docker instances on Router OS. 
    * [First video shows how to setup containers on your routerboard](https://www.youtube.com/watch?v=8u1PVouAGnk&t=113s). 
    *  [Video 2 shows you how to get PiHole working on a routerboard](https://www.youtube.com/watch?v=UMcJs4oyHDk).
* As part of Cloudflare's Birthday week, they announced a few things of interest for me today. I have signed up for early access to both. We see what the story is
    * [Introducing Cloudflare's free Botnet Threat Feed for service providers](https://blog.cloudflare.com/botnet-threat-feed-for-isp/)
    * [Monitor your own network with free network flow analytics from Cloudflare](https://blog.cloudflare.com/free-magic-network-monitoring/)
* 