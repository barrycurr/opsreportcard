---
layout: default
title: Do You Use Configuration Management Tools Like Ansible/Puppet/Chef?
has_children: true
nav_order: 16
parent: Automation
has_toc: false
---

{{ page.title }}
{: .fs-7 }

---

Config Management (CM) software is a tool that coordinates the configuration of machines. It might control the OS, the software, the service provided, or all of the above.

Before CM sysadmins manually made changes to machines. If you had to change 100 machines, you had 100 manual tasks to do. Smarter sysadmins would automate such a change.

Even smarter sysadmins realized that general tools for such automation would be even better. They invented automation frameworks with names Ansible, Puppet, Chef and others.

The hallmark of CM systems is that you describe what you want and the software figures out how to do it. What you want is specified in declarative statements like "hostA is a web server" and "web servers have the following packages and other attributes". The software turns that into commands that need to be executed. Another important attribute is that the declarations are generic ("install the commands in foo.sh as a cron job") but the CM system does the right thing for that computer's operating system (Selecting `/etc/crontab` vs. `/var/spool/cron`).

With CM, instead of manual changes, you change a configuration file and let the CM system do the work.

Local changes on a server are not ok. Any time you create a file like `/etc/crontab.bak` or `/etc/hosts.[today's date]` it is a red flag that you are doing it wrong.

Configuration management is the ultimate automation. You go from being the The Sorcerer's Apprentice to the puppet master. That's no Mickey Mouse idea.
