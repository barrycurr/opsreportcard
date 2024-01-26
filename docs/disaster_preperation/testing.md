---
layout: default
title: Are Your Disaster Recovery Plans Tested Periodically?
has_children: true
nav_order: 26
parent: Disaster Preperation
has_toc: false
---

{{ page.title }}
{: .fs-7 }

---

The last section was a bit of a lie. There aren't 4 reasons to do backups. There are 4 reasons to do restores.

Nobody cares about backups. People only care about restores. If you can figure out how to do restores without needing to do backups first I will lobby the Nobel committee to create a prize for sysadmins just so that you can be the first to receive it.

You don't know if backups are valid until you test them. Faith-based backup systems are not good. Hope sustains us but it is not an IT "strategy".

A full test involves simulating a total failure and doing a 'full restore'.

You won't know the real amount of time a restore takes until you try it. Restores from tape often take 10x longer than doing the backup. If you can do a full backup of your payroll server in 8 hours, then you have to be prepared to not cut paychecks for 80 hours in the event of a restore from scratch. That's more than 3 days.

If you are doing absolutely no tests then a little testing is better than nothing. Write a small script that randomly picks a server, then randomly picks a disk on that server, then randomly picks a file on that disk. The script should then create a ticket asking for that file to be restored (to a scratch location) as it existed 6 weeks ago. Have the script run automatically every week. This has a good chance of finding a server or disk that wasn't added to the backup schedule. Also, if you think doing these restores will be a lot of work for you, here's a secret: it won't use any of your time if your coworkers end up doing the ticket. Generate the ticket with enough random text that they don't know it is a drill.

To take this one step further, plan a "game day" where the disaster recovery plans are really put to the test. Pretend that certain people are dead and make sure the remaining people know how to fail-over services. Write scripts that document what tests will be performed. Either actually cause outages (disconnect the power or network cable) or play-act the scene: the "dead" person can proctor the test. "Ok, now lets suppose you got paged with this message. Tell me the commands you type and the actions you take." Another method is to permit your CEO to walk into the data center and unplug any cable of his or her choosing.
