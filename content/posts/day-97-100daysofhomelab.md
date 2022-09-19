---
title: Day 97 of 100daysofhomelab
date: 2022-09-19T21:30:00+00:00
tags: ["homelab", "100daysofhomelab"]
---
Day 97 (getting VERY close now!) of #100daysofhomelab and i have been playing with OSPF and AD.

* Mikrotik released a new update, [7.6beta7](https://mikrotik.com/download/changelogs/testing) of RouterOS, and 2 of the fixes are:
   - ospf - fixed checksum calculation;
   - ospf - improved logging when invalid configuration is detected;
* This now allows my OSPFv3 connection to connect! But i am still having issues actually sending routes. More tweaks required.
* Also managed to get my AD Syncing with Azure AD. My users don't match, but thats a job for tomorrow, probably.