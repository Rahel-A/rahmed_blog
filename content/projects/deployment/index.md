+++
title = "Homelab Configuration"
date = 2023-12-30

[taxonomies]
categories = ["homelab"]

[extra]
featured_image = "deployment.png"
featured_image_alt = "My Homelab configuration with Kubernetes and all of my servers/devices"
+++

My current Homelab configuration (Kubernetes deployment).
<!-- more -->

As I have not been working on a project, I have had plenty of time to experiment with Cloud Native technologies.
The TrueNAS Scale OS abstracts away the Kubernetes details, leading to ClickOps, but you still get some experience.
As I have interests in DevOps, I figured it was time that I learnt Kubernetes and started configuring my own system.
After three months of experimenting I took and passed [KCNA certification exam][1] without taking the course, so this route of learning proved quite educational.

I started experimenting with docker containers back in 2018 with a single Raspberry Pi.
Now I have a Raspberry PI running a few different containers related smart home, but also it is in my network's [DMZ][2] as the main point of entry

I do not have many the devices in the deployment yet, but the PI and my previously converted gaming PC into a NAS device have been pretty good so far.
Ideally I should separate some functions for improved security, but with the price hikes, scarcity, and what not, it is what it is...

{{ img(path="/2023/deployment-pi.svg", extended_width_pct=0.1, alt="Smart home Services", caption="Services running on PI", clickable=true) }}

At the time being I have not migrated the APPS running in TrueNAS to a Kubernetes node running in a VM on the TrueNAS.
This will be the plan:
{{ img(path="/2023/deployment-truenas.svg", extended_width_pct=1.0, alt="Media Services", caption="Services running on TrueNAS PC", clickable=true) }}

The Raspberry PI does not seem capable of being able to run more than a few containers of the types of services that I have configured in the network.
I had wished to run only media related services on the TrueNAS PC, but I migrated monitoring, and other non smart home related apps to the PC.
Thus, the overall deployment is as such:
{{ img(path="/2023/deployment.svg", extended_width_pct=0.9, alt="My Homelab deployment", caption="My current Homelab configuration", clickable=true) }}

I love configuring systems, so this has been an exciting journey.
It has been interesting to move my deployments to Kubernetes, and I will continue experimenting throughout 2024 and beyond.
I hope to eventually move into a cloud related role.

[1]: https://www.credly.com/badges/052b5593-910a-4201-ba42-30fe87d194ab
[2]: https://en.wikipedia.org/wiki/DMZ_(computing)
