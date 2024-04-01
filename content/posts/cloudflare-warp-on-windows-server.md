---
title: "Installing Cloudfalre Warp on Windows Server"
date: 2022-04-10T00:14:00+01:00
tags: ["homelab", "cloudflare", "godboxv3","windowsserver2022"]

---
I run Windows Server 2022 as my main OS on GodBoxV3, my workstation. When you try install [Cloudflare Warp](https://1.1.1.1) on it, it installs but fails to start. The issue is that Cloudflare Warp needs the Wireless LAN Service to be enabled. To enable, from an elevated Powershell Prompt, run

`Install-WindowsFeature wireless-networking`

Reboot the machine and Cloudflare Warp should now start.
