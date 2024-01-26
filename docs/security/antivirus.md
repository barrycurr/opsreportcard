---
layout: default
title: Do Desktops, Laptops, And Servers Run Self-Updating, Silent, Anti-Malware Software?
has_children: true
nav_order: 28
parent: Security Practices
has_toc: false
---

{{ page.title }}
{: .fs-7 }

---

Viruses and malware are a fact of life. If you think bad things don't happen to good people then we all must be bad people. Every machine needs anti-malware software now.

Every malware attack means work for you: cleaning up a failed machine, recovering data, consoling users over the loss of their data. It is a waste of time for you, an inexcusable disruption to your users. It is bad time management.

Anti-malware software needs to periodically update itself. Some anti-malware software pops up a big window that says, "There's a new update! Would you like me to install it?" This is an important window because the software's logo appears in it. If users know the brand of anti-malware being used, they can recommend it to friends. It helps the vendor's stock price if everyone knows their name. It doesn't matter that 9 times out of 10 the user clicks "no". Software that silently updates itself with no animated "update" notification does not have this benefit. How irresponsible of the company to not benefit their shareholders.

If you aren't sure, I'm being sarcastic.

There are many anti-malware products. The one you install should silently update itself.

It is your job to enforce the security policy and downloading updates is part of that policy. Delegating that responsibility to a user is wrong and possibly unethical. You don't ask a pedestrian, "Should I press the brakes and not run you over?" and you don't ask a user for permission to be less secure. Yes, we used to have 300 baud modems and downloading a virus definition file would take 30 minutes. You weren't even born then. You can't use that excuse. If you were around back then (like I was) then you are old enough to know better.

For similar reasons the anti-malware software should not be easily disabled by the user. Users will disable it for the most preposterous reasons. It is common for users to disable it in an attempt to speed up their computer. I once had a user that disabled it because "it attracts viruses to my machine". You see, he explained, when it was enabled it kept popping up windows warning of viruses. When he disabled it there were no warnings. Yes, people with such a gross misunderstanding of cause and effect do exist.

Anti-malware software used to be "would be nice" but now it is a requirement. These are my personal rules:

1. Anti-malware scanners must run on all machines including any server that contains user-controlled data: home directories, "file shares", web site contents, FTP servers, and so on.
1. Scanners must update automatically and silently. No user confirmation.
1. There must be a mechanism that lets you detect it has been disabled. They should "check in" with a central server so you can see which machines are no longer being updated.
1. Email must be scanned on the server, not on the client (or in addition to the client). Messages with malware must be dropped; messages with spam should be quarantined. You can't trust each individual machine to have the same, high-quality, up-to-date filter as you can maintain on your server. Stop the problem before it gets to the client.
