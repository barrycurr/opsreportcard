---
layout: default
title: Is The Network Core N+1?
has_children: true
nav_order: 24
parent: Disaster Preperation
has_toc: false
---

{{ page.title }}
{: .fs-7 }

---

An outage for one person is a shame. An outage of many people is unacceptable. Just like redundant disks is now a minimum, duplicate network connectivity is, too.

Yes, it is still expected that there is one link from a workstation to the first switch, but after that everything should be N+1 redundant. At a minimum, all trunks are dual-homed. At best, any one uplink, any one card, or any one network router/switch/hub can die and packets still get through.

LANs are generally designed as follows: The laptops/desktops in an office plug into the wall jack. Those connect to "access switches" which have many ports. Those access switches have "trunks" that connect to a hierarchy of "core switches" that scoot packets to the right place, possibly to egresses (the connections to other buildings or the Internet).

My rule is simple: The core has got to be redundant. It used to be a pricey luxury for the rich. Now it is a minimum requirement.

If your site isn't configured that way, you are living in the days when computers were useful without a network.

Exception: Sites small enough that they don't have a core. Even then all trunks should be redundant and a "spares kit" should exist for each kind of hardware device.
