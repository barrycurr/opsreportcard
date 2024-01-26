---
layout: default
title: Do Automated Administration Tasks Run Under Role Accounts?
has_children: true
nav_order: 17
parent: Automation
has_toc: false
---

{{ page.title }}
{: .fs-7 }

---

Often we set up automated procedures that run at predetermined times. For example, a script that validates a database once a night.

At some sites these scripts run as one of the sysadmins. When the sysadmin leaves the company those automated processes die.

Good sites run these scripts under some role account, often "root". However, it is safer to run them under an account with less privilege.
