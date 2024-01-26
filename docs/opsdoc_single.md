---
layout: default
title: OpsDoc Template (Single)
has_children: false
nav_order: 99
has_toc: false
---

{{ page.title }}
{: .fs-7 }

---

## Overview

### What Is It

?

### Why Do We Have It

?

### Primary Contacts

?

### Bug Reporting

?

### Design Documents

?

### Other Information

?

## Build

How to build the software that makes the service. Where to download it from, where the source code repository is, steps for building and making a package or other distribution mechanisms. If it is software that you modify in any way (open source project you contribute to or a local project) include instructions for how a new developer gets started. Ideally the end result is a package that can be copied to other machines for installation.

## Deploy

How to deploy the software. How to build a server from scratch: RAM/disk requirements, OS version and configuration, what packages to install, and so on. If this is automated with a configuration management tool like cfengine/puppet/chef (and it should be), then say so.

## Common Tasks

Step-by-step instructions for common things like provisioning (add/change/delete), common problems and their solutions, and so on.

## Pager Playbook

A list of every alert your monitoring system may generate for this service and a step-by-step "what do to when..." for each of them.

## Disaster Recovery

Disaster Recovery Plans and procedure. If a service machine died how would you fail-over to the hot/cold spare?

## Service Level Agreement

> The (social or real) contract you make with your customers. Typically things like Uptime Goal (how many 9s), RPO (Recovery Point Objective) and RTO (Recovery Time Objective).

| SLA Tags         | Setting |
|------------------|---------|
| System-Severity  | Medium  |
| Patching         | Monthly |
| RACI Accountable | ?       |
| RACI Responsible | ?       |
| RACI Informed    | ?       |
| Reboot           | Yes     |

### Contract

?

### Social Contract

?

### Uptime Expectation

> 99%, 99.9%, etc

### Recovery Point Objective

> The maximum amount of data – as measured by time – that can be lost after a recovery from a disaster, failure, or comparable event before data loss will exceed what is acceptable to an organization

### Recovery Time Objective

> The maximum acceptable time that an application, computer, network, or system can be down after an unexpected disaster, failure, or comparable event takes place

## In-House Information

> If this is something being developed in-house, the 8th tab would be information for the team: how to set up a development environment, how to do integration testing, how to do release engineering, and other tips that developers will need. For example one project I'm on has a page that describes the exact steps for adding a new RPC to the system.

### How To Setup a Development Environment

?

### Integration Testing

?

### Release Engineering

?

### Other Tips and Information

?
