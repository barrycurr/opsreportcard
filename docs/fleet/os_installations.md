---
layout: default
title: Is OS Installation Automated?
has_children: true
nav_order: 20
parent: Fleet Management Process
has_toc: false
---

{{ page.title }}
{: .fs-7 }

---

Automated OS installations are faster, more consistent, and let the users do one more task so you don't have to.

If OS installation is automated then all machines start out the same. Fighting entropy is difficult enough. If each machine is hand-crafted, it is impossible.

If you install the OS manually, you are wasting your time twice: Once when doing the installation and again every time you debug an issue that would have been prevented by having consistently configured machines.

If two people install OSs manually, half are wrong but you don't know which half. Both may claim they use the same procedure but I assure you they are not. Put each in a different room and have them write down their procedure. Now show each sysadmin the other person's list. There will be a fistfight.

Users see inconsistency as incompetence. If new machines always arrive with a setting that isn't to their liking they know how to change that setting and are happy. If half the time that setting is one way and half the time it is another way, they lose confidence in the system administrators. What bozos are installing this stuff?

If you can re-install the OS automatically, so can the users. Now you have one less thing to do. Automation that saves you time is great. Automation that lets other people do a task is even better.

Not being able to easily wipe and reload a machine is a security issue. A machine should be wiped and reloaded when a "hand me down" computer moves from one user to another. If this process isn't "friction free" there is temptation to "save time" by not doing it.
