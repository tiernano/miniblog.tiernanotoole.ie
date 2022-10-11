---
title: Day 119 of 100daysofhomelab
date: 2022-10-11T20:26:46+01:00
tags: ['homelab', '100daysofhomelab']
---
Day 119 of #100daysofhomelab and there has been some big (and small) changes on the network.

* Moved my [Mikrotik](https://mikrotik.com) router from Hyper-V to Proxmox. Slightly lower spec CPU ([Celeron J4125](https://ark.intel.com/content/www/us/en/ark/products/197305/intel-celeron-processor-j4125-4m-cache-up-to-2-70-ghz.html) vs [Xeon Gold 6138](https://ark.intel.com/content/www/us/en/ark/products/120476/intel-xeon-gold-6138-processor-27-5m-cache-2-00-ghz.html)) but has a direct connection to both the PPPoE link for the FTTH connection, along with the Cable Modem. So, less stuff in-between to go wrong.
* Fixed Prometheus to point at the new [Mikrotik Exporter](https://github.com/nshttpd/mikrotik-exporter) location. Had to tweak some IPs that were missing from the last move.
* Still in the process of IP Renumbering for my ASN move... Hope to get more time this week or this weekend to sort it out fully.
