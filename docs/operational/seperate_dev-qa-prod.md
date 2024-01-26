---
layout: default
title: Do You Have Separate Development, QA and Production Systems?
has_children: true
nav_order: 14
parent: Operational Practices
has_toc: false
---

{{ page.title }}
{: .fs-7 }

---

Developers do their work on their development servers. When they think it is done packages are built and installed on the QA system. If QA and UAT (User Acceptance Testing) approves, the same packages are used to install the software on the production systems.

This is Sysadmin 101, right?

Then why do I constantly meet sysadmins whose management won't let them do this? If your management says "it costs too much to have a second machine" they're beyond hope. QA isn't expensive. You know what is expensive? Downtime.

Experimental changes on the live server isn't just bad, in SOX environments it is illegal. Letting developers develop on the live servers is right out!

The QA system need not be as expensive as their live counterpart. They don't have to be as powerful as the live system, they can have less RAM and disk and CPU horsepower. They can be virtual machines sharing one big physical machine.

Obviously if scaling and response time are important it is more likely you'll need a QA system that more closely resembles the live system.
