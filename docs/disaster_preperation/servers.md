---
layout: default
title: Can Your Servers Keep Operating Even If 1 Disk Dies?
has_children: true
nav_order: 23
parent: Disaster Preperation
has_toc: false
---

{{ page.title }}
{: .fs-7 }

---

It used to be that if there was one broken component in a computer, you had an outage. In fact, one component failure equaled one outage. One disk dies and you spend the day replacing it and restoring data from the backup tapes. Too bad if you had hoped to get some work done, too bad if you planned to be at the company picnic that day. One failed disk ruins your whole day; just like nuclear war.

Today things are different. We build "survivable systems". If a disk is part of a mirrored pair then one of those disks can fail and there is no outage. There is only an outage if it's mirrored partner also breaks. Statistically that gives you hours, possibly days, to replace the broken disk before a user-visible outage would happen. Rushing to replace a disk is a better use of your time than spending a day restoring data from tape.

When you do this you have decoupled "component failure" from "outage". Life is better.

RAID used to be expensive and rare. A luxury for the rich. Now it is common, inexpensive, and often free (when done in software). Did I say common? I meant mandatory. Spending a day restoring data off tape isn't just a sign of bad planning, it's bad time management. It is a waste of your time to spend the day consoling a distraught user who has lost years, months, or even just hours, of work. It isn't heroic. It is bad system administration. Let's not forget the bigger waste of time for your users, possibly hundreds of them, waiting for their data to be restored off a backup tape. Disk failures are not rare. Why did you build a system that assumed they are?

The MTBF of a typical server drive is 1.5 million hours. If you have 1,000 disks, expect a failure every 2 months. If you have 10,000 disks expect a failure every week. Are you really planning to spend an entire day restoring data from tape that often?

My rule of thumb is simple: For small servers the boot disk should be mirrrored and any disk with user data should be RAID1 or higher.

Boot disk: I recommend mirroring the boot disk of every server because it is usually impossible to rebuild from scratch. Server boot disks tend to accumulate "stuff". Over the years many software packages may be installed. New drivers, patches and kludges may exist that aren't documented. The configuration is more a history of the company than some well-planned design. In a perfect world none of this would be true. Every machine should be reproducible though an automated system. Alas, that is the goal but we aren't there yet. The primary exception is clusters of homogenous machines like HPC environments or Google or Yahoo!. Alas, dear reader, I bet that isn't your situation. In fact, I bet that even at Google and Yahoo! the Windows server that runs keycard system that lets people in and out of the buildings is exactly the worst-case scenario that needs a mirrored boot disk.

Yes, you could probably rebuild such a server in a day if you are lucky, but a RAID1 controler is less than that in salary if you work minimum wage.

User data: I recommend RAID1 or higher for user data just because it is so inexpensive that not doing it is embarrassing. By the way... you do know that RAID6 is the minimum for 2T disks and larger, right? It is professionally negligent to use RAID5 on such disks. RAID6 or RAID10 is the minimum; at least for now, but I digress.

The exceptions to all this is any place where the service can keep running if individual components die whether the redundency is at the disk level, the machine level, or the data center level. Also, data that can be reconstructed from scratch within the SLA. Here are some examples:

- The use of a fancy redundant file systems like the Google File System (GFS). GFS stores all data in at least 3 places. IBM's GPFS Native RAID (GNR) does something similar.
- "Scratch and temp space" where users know it could go away at any time.
- Video or other read-only data that could, if lost, be re-read from media.
- The data is a read-only copy of data found elsewhere. Though if you are replicating for speed, RAID5 might give you a performance boost because it uses more spindles.
- Disposable machines. For example, a static image web server or a DNS "secondary and cache"-only server that can be rebuilt quickly and automatically. If you have hundreds of them the savings from not buying RAID cards can be dramatic.
