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

All T1Pal code goes into this github code repository.   By "code" we include the following artifacts:

* software of any particular language (javascript, Ruby, PHP, C++, BASH)
* configuration files (e.g. nginx configuration files)
* service definition files (e.g. docker files, .yaml files for Kubernetes, HOLM charts)

Services provided by Docker containers shall be "built" using Docker files that is controled by a docker command line or script.
Configuration parameters for all functions shall be provided within the Docker file.

A specific BASH script shall be used to trigger the transfer and activation of new product instances.

T1Pal uses a number of external services that are configured manually and operationally accessed using a well-defined
API.  These including stripe.com, servicebot.io, MongoDB, postgresdb, DNS, and Digital Ocean hosting services.
It is the goal of T1Pal to leverage all such public services to the maximum extent possible, subject
to operational cost, reliability, security, and performance requirements.



