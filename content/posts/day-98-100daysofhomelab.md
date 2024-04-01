---
title: Day 98 of 100daysofhomelab
date: 2022-09-20T20:00:00+00:00
tags: ["homelab", "100daysofhomelab"]
---
Day 98 of #100daysofhomelab and ive been working on Cloudflare Workers stuff and trying to fix my Azure AD Sync.

* I use [Wordpress](https://wordpress.org) on [my main blog](https://tiernanotoole.ie) and the [AS204994](https://as204994.net) site with the [Cloudinary](https://cloudinary.com/invites/lpov9zyyucivvxsnalc5/odc5hvptjxifri3jusn9?t=default) Plugin for images. I am trying to rewrite the URLs to use a different domain for image hosting. It will do caching of images, saving bandwidth on Cloudinary and hopefully making things faster... So far, not working as planned, but getting closer...
* I have some (very minor, mostly caching and logging edits) edits to the original [Cloudflare Workers code for the Cloudinary Proxy](https://github.com/wesbos/cloudflare-cloudinary-proxy) from [wesbos](https://github.com/wesbos).
* looks like my Azure AD Sync failed at some stage, so digging though that to fix it.
* Also, seems something on the network is acting up... I think this might be appropriate...

{{< cloudinary "miniblog/download.jpg" "200" "it was dns" >}}
