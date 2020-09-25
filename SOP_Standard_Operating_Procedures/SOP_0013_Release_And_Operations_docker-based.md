---
repository: "github.com/ehwest/mdn_qms"
folder: "mdn_qms/SOP_Standard_Operating_Procedures"
title: "SOP_0013_Docker_Release_and_Operations.md"
document_id: "SOP-0013"
authors:
- github.com/ehwest
approvers:
- github.com/bewest
revision: "05"
approval_date: "2020-07-18"
effective_date: "2020-07-18"
content_type: concept
description: "SOP 0013 Docker Release and Operations"
---

**T1Pal Code Repository and the Gitflow Process**

Any and all software released as part of T1Pal shall first be introduced to (i.e. created on) the T1Pal platform
as a branch of the T1Pal github code repository.  All software is created first on either of the following
two branches:  

1. <named> "**feature**" branch -- for software not yet associated with a relase.
2. "**development**" branch -- for software definitely targeted to a particular relase.

Following the "**gitflow**" process, all T1Pal "code" goes into this github code repository.   
By "code" we include the following artifacts:

* software of any particular language (javascript, Ruby, PHP, BASH)
* configuration files (e.g. nginx, apache web server configuration files)
* service definition files (e.g. docker files, .yaml files for Kubernetes, HOLM charts)
* Instructions for manually configuring services from a particular platform service provider (e.g. Digital Ocean servers, AWS, MongoDB, Redis, postgresdb)

Component services built on Docker containers shall be "built" using Docker files controled by 1) a docker command-line or 2) a script.

In either case, the command-line and/or the script shall itself be included in the development github repository.
Configuration parameters for all functions of a docker container shall be provided within the Docker file, and stored in the github repository.

A specific BASH script shall be used to trigger the transfer and activation of new product instances.

T1Pal uses a number of external services that are configured manually and then operationally accessed using a well-defined
API.  These including stripe.com, servicebot.io, MongoDB, postgresdb, DNS, Kubernetes clusters, and Digital Ocean hosting services.
It is the goal of T1Pal to leverage all such public services to the maximum extent possible, subject
to operational cost, reliability, security, and performance requirements.

Step-by-step procedures to manually create and utilize any external service shall be documented in the T1Pal development github repository in .md format.

**Release Process**
A "release" of new or changed software to production amounts to promoting the "staging" branch of the github repository to the "master" branch of the github repository, where it can be tested prior to final release.

The production branch of the repository "should" exactly match the deployed production software.

The release process generally involves logging into a production server so as to remotely "check out" the correct development branch from the github repository.
Each component of the T1Pal system has it's own "repo" that has a development, staging, feature, and release branches.   

The "staging" branch of the github repository contains the tested final version to be promoted to production.   The "staging" branch is subject to extensive testing and is only available to operations staff.

A "run-book" is a check-list style document (stored in the github repository) that provides all of the methods and procedures needed to promote a "staging" branch to the "production" branch and test for correct operation.   Testing of the run-book is also done in the staging environment.

Prior to checking out the production software on a T1Pal component (from the master repo), a data transition script may be required to prepare the production environment with the right data, in the right schema.  A backup of the production data must be done for all software changes impacting data.

**Operations Management**

The T1Pal solution is in fact an interworking set of services that are each somewhat independent of each other.   The run-book described above
is used to direct operations staff to reports,  displays of data flows, lists of resources consumed, and response times for specified components.

The operations staff must monitor all displays and reports continuously 24 x 7 x 365 and at the same time monitor trouble ticket complaints.

In the event of an outage of any kind, the outage must be documented on freshstatus.com web site so as to alert customers subscribing to that service.
https://t1pal-995.freshstatus.io/admin/status    Any and all observed impairments to any T1Pal components should be entered into a trouble ticket.  The trouble ticket system is configured to receive emails directed to support@t1pal.com   The trouble ticketing system is at  t1pal.helpy.io






