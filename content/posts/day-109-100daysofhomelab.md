---
date: 2022-10-01T23:29:24+01:00
title: Day 109 of 100daysofhomelab
tags: ["100daysofhomelab","homelab"]
---
Day 109 of #100daysofhomelab and I have done some tweaks to PipeDream, got some new switches and ordered a new HDMI monitor for my camera...

* Tweets from my miniblog (this one) get posted to twitter within 2 hours of posting, but they don't include the #100daysofhomelab due to some issue with Hugo i haven't figured out. They are posted using [PipeDream](https://pipedream.com). So, i tweaked Pipedream to now run a [NodeJS](https://nodejs.org/en/) script to fix the title to include #100daysofhomelab. The code is simple enough: `string.replace(' 100daysofhomelab', ' #100daysofhomelab')`. That space in front makes sure if i do ever fix hugo, i wont be putting 2 hashtags in...
* On a more homelab note, i got my hands of 2 EdgeSwitch 48 Pros. They are non POE, but have 2 10Gb uplinks. both will go in the [Cloudshed](https://cloudshed.net) with a fiber link between it and the house. More hopefully next week!
* I have ordered an [Neewer F100 7 Inch Camera Monitor](https://geni.us/Druv) to attach to my [Blackmagic Pocket 6k](https://geni.us/5JLf). Its meant to arrive on Monday, so hopefully that will be timing enough for a video on the Cloudshed!