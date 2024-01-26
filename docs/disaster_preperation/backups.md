---
layout: default
title: Are Your Backups Automated?
has_children: true
nav_order: 25
parent: Disaster Preperation
has_toc: false
---

{{ page.title }}
{: .fs-7 }

---

This question assumes you are doing backups. You are doing backups, right?

You need backups for 4 reasons:

1. Oops, I deleted a file.
1. Ooops, the hardware died.
1. Oh no, the building burned down.
1. Archives.

Each of these may require different backups methodologies.

1. Is solved by snapshots in the short-term but not in the long term. Sometimes a file is deleted and needs to be restored much later. Simple snapshots will not help. RAID does not help in this situation. RAID is not a backup mechanism. If someone deletes a file by mistake, RAID will dutifully replicate that mistake to all mirrors. You will have a Redundant Array of Incorrect Data.

1. Sounds like RAID will help, but remember that a double-disk failure can mean you've lost the entire RAID1 mirror or RAID5 set. RAID10 and RAID6 lose all data in a triple-disk failure. These things happen. You are one clumsy electrician away from having all disks blow up at once. Really.

1. Is often called "disaster recovery". Off-site backups, whether on tape or disk, are your only hope there.

1. Is often for compliance reasons. The technology to make the backup is often the same as Situation 3 but the retention time is usually different. If some other department is requiring these for compliance, they should pay for the media.

For any of these reasons the process must be automated. As the building burns down you don't want to have to inform management that the data is lost because "I was on vacation" or "I forgot".
