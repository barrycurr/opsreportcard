---
layout: default
title: Do You Have A Pager Rotation Schedule?
has_children: true
nav_order: 13
parent: Operational Practices
has_toc: false
---

{{ page.title }}
{: .fs-7 }

---

Do you have a pager rotation schedule or are you a sucker that is simply
on-call forever?

An on-call rotation schedule documents who is "carrying the pager" (or
responsible for alerts and emergencies) at which times.

You might literally "pass the pager", handing it to the next person
periodically, or everyone might have their own pager and your monitoring
system consults a schedule to determine who to page. It is best to have
a generic email address that goes to the current person so that
customers don't need to know the schedule.

A rotation schedule can be simple or complex. 1 week out of n (for a
team of n people) makes sense if there are few alerts. For more complex
situations splitting the day into three 8-hour shifts makes sense.
"Follow the sun" support usually schedules those 8-hour shifts such that
a global team always has a shift during daylight hours. You might take a
week of 8-hour shifts each n weeks if your team has 3n people. The
variations are endless.

This schedule serves many people: You, your customers, management and
HR.

It serves you well because it lets you plan for a life outside of work.
I put the highest priority on having a good work-life balance. If you
don't have a good work-life balance, and you don't have a rotation
schedule, physician heal thy self.

The rotation improves service to customers because it takes the "chaotic
panic of trying to find a sysadmin" and makes it easy and predictable.

It serves management because it gives them confidence that the next
emergency won't happen while everyone is "away".

It serves HR since, of course, your company gives compensation time or
pay as required by law. If your schedule is in machine-readable format,
a simple script can read it to generate reports for the payroll
department.

If you think you don't have a schedule then it is "24x7x365" and you are
a sucker. (But that doesn't mean you can answer "yes" for this
question.)
