---
layout: default
title: In Your Bugs/Tickets, Does Stability Have A Higher Priority Than New Features?
has_children: true
nav_order: 8
parent: Modern Team Practices
has_toc: false
---

{{ page.title }}
{: .fs-7 }

---

Adding new features is more fun than fixing bugs. Sadly we can't be fun
here.

Mature teams prioritize bugs this way:

- security (highest)
- stability
- bugs
- performance
- new features (lowest)

You have to fix stability before you add new features. Security issues
are high priority stability issues.

One of the principles promoted by Mark Burgess is "seek stability, then
new features". Some changes we make add features while others improve
stability. The order should be feature, stability, feature, stability,
feature, stability. Not feature, feature, feature, OMG!, stability,
stability, stability. Make things stable before proceeding to the next
awesome feature.

Doctors understand this. In a hospital emergency room a patient is
stabilized first. You don't help someone recover from the flu if they
are bleeding to death.

The priority of "performance bugs" is up for debate. In some places
performance is the same as stability.
