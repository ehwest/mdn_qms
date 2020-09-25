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

Any and all software released as part of T1Pal shall first be introduced to the T1Pal platform
as a branch of the T1Pal github code repository.  It may be introduced in either of the following
two branches:  

1. a <named> feature branch 
2. a development branch

All T1Pal "code" goes into this github code repository.   
By "code" we include the following artifacts:

* software of any particular language (javascript, Ruby, PHP, BASH)
* configuration files (e.g. nginx, apache web server configuration files)
* service definition files (e.g. docker files, .yaml files for Kubernetes, HOLM charts)

Component services built on Docker containers shall be "built" using Docker files controled by a docker command-line or script.
In either case, the command-line and/or the script shall itself be included in the development github repository.
Configuration parameters for all functions of a docker container shall be provided within the Docker file, and stored in the github repository.

A specific BASH script shall be used to trigger the transfer and activation of new product instances.

T1Pal uses a number of external services that are configured manually and then operationally accessed using a well-defined
API.  These including stripe.com, servicebot.io, MongoDB, postgresdb, DNS, Kubernetes clusters, and Digital Ocean hosting services.
It is the goal of T1Pal to leverage all such public services to the maximum extent possible, subject
to operational cost, reliability, security, and performance requirements.

Step-by-step procedures to manually create and utilize any external service shall be documented in the T1Pal development github repository in .md format.

A "release" of new or changed software to production amounts to promoting the "staging" branch of the github repository to the "production" branch of the github repository.
The production branch of the repository exactly matches the production software.   The "staging" branch of the github repository contains the tested final version to be promoted to production.   The "staging" branch is subject to extensive testing and is only available to operations staff.

A "run-book" is a check-list style document (stored in the github repository) that provides all of the methods and procedures needed to promote a "staging" branch to the "production" branch and test for correct operation.   Testing of the run-book is also done in the staging environment.




