---
title: Simple Home Server Setup with Samba (and OpenWRT)
description: Simple Home Server Setup with Samba (and OpenWRT)
date: 2025-04-02
draft: false
---
# OpenWRT setup (installing and uninstalling)
### Installing OpenWRT
In my last post about networking ([[VPNs, Home router setup, starting my networking journey]]) I talked about why I initially choose to use OpenWRT and what it offers compared to stock router firmware.
I will not be providing a how-to guide on this as there is great information on the internet: Use [this video to](https://www.youtube.com/watch?v=pa7VhElcExI&t=86s&ab_channel=Krisseck) get started (how to install), or [this video](https://www.youtube.com/watch?v=7cxiYmn3OTU&t=190s&ab_channel=VanTechCorner) for a complete overview of the features that OpenWRT offers.
I installed OpenWRT on a NETGEAR R6700v2 which I got on eBay for $25.
After installing OpenWRT I made some changes including the following:
- Changed passwords on router for router login and wi-fi login(s).
- Hid Wi-Fi names from network (ESSID)
- Set up static IP addresses for devices.
- Port forwarding (if needed)
I was not able to get the port forwarding to work. At first I thought this was an OpenWRT issue but after uninstalling it and installing the stock firmware (see next section), it still did not open the ports. My guess is this has something to do with the apartment internet but I am not 100% sure. If you have your router setup in your home this should definitely work.
### Uninstalling OpenWRT and Installing Stock Firmware
I ended up uninstalling openwrt using [this method](https://www.youtube.com/watch?v=cEXbTVi9OdA). This should work (on most if not all) NETGEAR routers. I am not sure about other brands. The tutorial also goes over how to install the stock firmware back onto the router.
After installing the stock firmware I would recommend making the following changes:
- Chang passwords on router for router login and wi-fi login(s).
- Set up static IP addresses for each device on your network.
# Basic Server Setup Guides
### Samba
[Used Samba on Linux computer to create a file share server for computers on the local network to connect into](https://www.youtube.com/watch?v=oRHSrnQueak&ab_channel=ChrisTitusTech)
### Remote Desktop
[Remote desktop into linux computer from mac](https://www.youtube.com/watch?v=_0aP2s8G5Js&ab_channel=Tricknology)
