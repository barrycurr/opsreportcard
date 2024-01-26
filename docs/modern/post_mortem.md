---
layout: default
title: Do You Have A "Post-Mortem" Process?
has_children: true
nav_order: 10
parent: Modern Team Practices
has_toc: false
---

{{ page.title }}
{: .fs-7 }

---

After a failure do you write up what happened so you can learn from it or do you just hope nobody notices and that it will all go away?

A good post-mortem (PM) includes a timeline of what happened, who was affected, what was done to fix it, how was business affected, and a list of proposed solutions to prevent this problem from happening again. Each proposal should be filed as a bug or ticket so they can be tracked to completion.

Doing PMs consistently builds a more stable environment. After each outage come up with at least one preventative measure. Can your monitoring system detect the situation so you know about it before users do? Can you detect precursors to the problem? Often systems have a way to run a battery of tests on new configurations before they are adopted ("pre-submit scripts" in source code repositories, for example). Are there tests you can add that will detect the typo that created the outage?

A post-mortem is not about blaming and shaming. In a good sysadmin culture you are comfortable with putting your name in the "what went wrong" section. You are taking a leadership role by educating people so they don't make the same mistake.

If your management uses PMs to find who to punish, they don't understand that operations isn't about doing things perfectly; it is about doing things better and better every day. Any manager that fires a person because of a non-malicious outage is going to run their company into the ground.

The PM should be published for all to see. You may be embarrassed and concerned that you are "airing your team's dirty laundry" but the truth is that if you consistently do this your users will respect you more. Transparency breeds trust.

Of course, to really develop confidence all those bugs and tickets filed as a result need to actually get worked on.
