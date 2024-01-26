---
layout: default
title: Does Each Service Have An Opsdoc?
has_children: true
nav_order: 11
parent: Operational Practices
has_toc: false
---

{{ page.title }}
{: .fs-7 }

---

Your DNS server dies. You rebuild it because you know how. Cool, right? You need to compile the newest version of BIND and install it, and you do it because you know how, right? When the monitoring system reports that error that happens now and then, you know how to fix it, right? You know how to do all this. Why write anything down?

Here's why:

Will you remember how to do these things 6 months from now? I find myself having to re-invent a process from scratch if I haven't done it in a few months (or sometimes just a few days!). Not only do I re-invent the process, I repeat all my old mistakes and learn from them again. What a waste of time.

Will you remember how to do these things when the pressure is on? My memory works worse during an emergency.

What about when you aren't around? How can you take a relaxing vacation if you feel burdened? You can't complain to be over-worked and unable to share your work with others if you haven't created a way to share the workload.

What about new people on the team? Should they learn how to do these things by watching you do it or can they learn on their own? If they can learn on their own and only bother you when they get stuck it saves you time and makes you look less like the information hording curmudgeon that you don't want to be. In fact, it makes people feel welcome and included if their new team has these kind of tasks documented.

How can your manager promote you or put you on a new and more interesting project if you are the only person with certain knowledge?

Each service should have certain things documented. If each service documents them the same way, people get used to it and can find what they need easier. I make a sub-wiki (or a mini-web site, or a Google Sites "Site") for each service:

Each of these has the same 7 tabs: (some may be blank)

1. [Overview](/docs/opsdoc/overview.md): Overview of the service: what is it, why do we have it, who are the primary contacts, how to report bugs, links to design docs and other relevant information.

1. [Build](/docs/opsdoc/build.md): How to build the software that makes the service. Where to download it from, where the source code repository is, steps for building and making a package or other distribution mechanisms. If it is software that you modify in any way (open source project you contribute to or a local project) include instructions for how a new developer gets started. Ideally the end result is a package that can be copied to other machines for installation.

1. [Deploy](/docs/opsdoc/deploy.md): How to deploy the software. How to build a server from scratch: RAM/disk requirements, OS version and configuration, what packages to install, and so on. If this is automated with a configuration management tool like cfengine/puppet/chef (and it should be), then say so.

1. [Common Tasks](/docs/opsdoc/common.md): Step-by-step instructions for common things like provisioning (add/change/delete), common problems and their solutions, and so on.

1. [Pager Playbook](/docs/opsdoc/pager_playbook.md): A list of every alert your monitoring system may generate for this service and a step-by-step "what do to when..." for each of them.

1. [Disaster Recovery](/docs/opsdoc/disaster_recovery.md): Disaster Recovery Plans and procedure. If a service machine died how would you fail-over to the hot/cold spare?

1. [SLA](/docs/opsdoc/sla.md): Service Level Agreement. The (social or real) contract you make with your customers. Typically things like Uptime Goal (how many 9s), RPO (Recovery Point Objective) and RTO (Recovery Time Objective).

1. [In House Information](/docs/opsdoc/in_house_info.md): If this is something being developed in-house, the 8th tab would be information for the team: how to set up a development environment, how to do integration testing, how to do release engineering, and other tips that developers will need. For example one project I'm on has a page that describes the exact steps for adding a new RPC to the system.

Be a hero and create the [template](../opsdoc/) for the rest of your team to use. Document a basic service like DNS to get started. Then do this for a bigger service. Create the skeleton so others can use it as a template and just fill in the missing pieces. Get in the habit of starting a new opsdoc any time you begin a new project.
