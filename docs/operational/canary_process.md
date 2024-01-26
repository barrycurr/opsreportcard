---
layout: default
title: Do Roll-Outs To Many Machines Have A "Canary Process?"
has_children: true
nav_order: 15
parent: Operational Practices
has_toc: false
---

{{ page.title }}
{: .fs-7 }

---

Suppose you have to roll out a change to 500 machines. Maybe it is a new
kernel. Maybe it is just a small bug-fix.

Do you roll it out to all 500? No. You roll it out to a small number of
machines and test to see if there are problems. No problems? Roll out to
more machines. Then more and more until you are done.

These early machines are called "canaries".

> _The classic example of animals serving as sentinels is the canary in
> the coal mine. Well into the 20th century, coal miners in the United
> Kingdom and the United States brought canaries into coal mines as an
> early-warning signal for toxic gases including methane and carbon
> monoxide. The birds, being more sensitive, would become sick before
> the miners, who would then have a chance to escape or put on
> protective respirators. Source: Wikipedia_

Here are some canary techniques:

- One, Some, Many:

Do one machine (maybe your own desktop), do some machines (maybe your
co-workers), do many machines (larger and larger groups until done.) Any
single failure means you stop the upgrade, roll back the change, and
don't continue until the problem is fixed.

- Cluster Canary:

Upgrade 1 machine, then 1% of all machines, then 1 machine per second
until all machines are done. (Typical at Google and sites with large
clusters) This procedure can be done manually but if you use a
configuration management system, the ability to do canaries should be
"baked in" to the system.
