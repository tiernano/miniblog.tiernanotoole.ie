---
title: Day 120 of 100daysofhomelab
date: 2022-10-12T21:07:45+01:00
tags: ['100daysofhomelab','homelab']
---
Day 120 of #100daysofhomelab and I *nearly* got Bird 2.0 working... Then it failed...

I am not 100% sure what I am doing wrong here, but essentially, on old Bird 1.6, you could create static routes like:

    protocol static {
        #send traffic to own server external IPs direct to gateway peer.
        route x.x.x.x/32 via y.y.y.y;
    }

This would then have a static route set for that /32 going though that IP. The reason is because i would have something like as follows:

    protocol kernel {
        scan time 90;
        import all;
        merge paths on; #ECMP
        export filter {
                if (source = RTS_STATIC || source = RTS_DEVICE) then accept; #static and device routes
                if (source = RTS_BGP) then {
                        # Export some routes to the kernel routing table
                        
                        if (bgp_path.len = 0) then
                        {
                                accept; # Internal Routes
                        }
                        else
                        {
                                krt_prefsrc = OWNSRC;
                                accept;
                        }
                        reject;
                }

                accept;
        };   # Actually insert routes into the kernel routing table
    }

essentially, that would first, setup ECMP for routes that have multiple same length hops. Then, it starts doing exporting of routes to the kernel. The line for static and device routes exports them to the kernel, but does not change their preferred source (more on that in a sec). Internal routes does the same. everything else is set to use `OWNSRC` (an IP from my /24) as the source of that, so any traffic to that comes from that IP.

Problem is, that doesn't seem to work on Bird 2... or I have screwed up something somewhere... More digging required...
