---
layout: default
title: Are User Requests Tracked Via A Ticket System?
has_children: true
nav_order: 1
parent: Public Facing Practices
has_toc: false
---

{{ page.title }}
{: .fs-7 }

---

This is so basic it pains me that I have to explain it.

Humans can't remember as well as computers. Expecting sysadmins to
remember all user requests is the direct route to dropping requests.

Keeping requests in a database improves sharing within the team. It
prevents two people from working on the same issue at the same time.
It enables sysadmins to divide work amongst themselves. It enables
passing a task from one person to another without losing history. It
lets a sysadmin back-fill for one that is out, unavailable or on
vacation.

It enables better time management. Every interruption a sysadmin
receives sets his or her work back 7 minutes. A ticket system prevents
interruptions from users that want to make requests or ask for status
of requests. It lets sysadmins prioritize their work instead of
responding to the loudest complainer.

It lets managers be better managers. Stalled requests become visible
so that managers can intervene. It reveals trends and frequent
requests so that they may be eliminated via new automation or process
improvements. Micro-managers can get the information they want via
software rather than bothering their sysadmins. It replaces "user
whining" with evidence-based discussions: If a request really has
taken too long the manager can properly address the issue; if the user
only perceives the issue is taking a long time the evidence will shut
them down. If they claim "it's been a problem for months but I only
opened the ticket yesterday" then the manager has an... opportunity to
educate the user about the non-existence of time-travel, mind-reading,
and other supernatural powers.

It helps you identify systemic problems. I once had a boss query the
ticket system and discover that 3 out of our 1,000 users opened 10% of
all tickets. A little investigation and we were able to solve the
fundamental issues causing this.

It helps users help themselves. Frequently when a user writes down
what their problem is they realize what the solution is and no ticket
is opened. When this doesn't happen, it helps them think through the
problem so they can communicate it more clearly, which makes the
actual transaction more efficient.

I spent the 1990s being the "radical" encouraging people to set up
ticket systems. I spend the 200xs pleased to see it become accepted
practice. We are well into the third decade. If you don't have a way
to track user requests at this point shame on you.
