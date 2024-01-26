---
layout: default
title: Do Automated Processes That Generate E-Mail Only Do So When They Have Something To Say?
has_children: true
nav_order: 18
parent: Automation
has_toc: false
---

{{ page.title }}
{: .fs-7 }

---

Do you know the story of:
> "The Boy Who Cried Wolf"?

What about:
> "The cron job that everyone ignored because it blasted everyone twice a day, and nobody noticed when it started to report problems."

My rule is simple:

- If it needs human action now: Send a page/SMS.
- If it needs action in 24 hours: Create a ticket.
- If it is informational: Log to a file.
- Output nothing if there is no information.

While sending a page and creating a ticket might be done via email, the point is that email is not a good mechanism for this. Either may CC: you, but email is not the primary mechanism.

The worst case situation is a system that sends log messages to everyone on the sysadmin team via email. Your email system is not a good log archive.

True story: A friend in NYC worked at a site where all automated processes sent their output as email to root@the-company-domain. "root" was a mailing list that went to all the sysadmins in the company. It was a constant flood of messages. Sysadmins at this company literally could not read email. No amount of filtering would be enough. As a result, the sysadmins for this company used their personal email accounts for all communication, even stuff that was work-related. What company was this? A major email provider that is no longer in business. (I wonder what other bad decisions helped put them out of business?)
