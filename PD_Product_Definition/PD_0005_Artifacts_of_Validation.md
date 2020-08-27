---
repository: "github.com/ehwest/mdn_qms"
folder: "PD"
title: "PD_0005_Artifacts_of_Validation.md"
document_id: "PD_0001"
authors:
- github.com/ehwest
approvers:
- github.com/bewest
revision: "05"
approval_date: "2020-08-24"
effective_date: "2020-08-24"
description: "T1Pal Artifacts of Validation and Verification"
---

This document is intended to capture the results of Verification and Validation activities.
As such, it will be populated with data as those tests are carried out.


|Micro_Service_ID|Micro_Service Description|APIs Tested|Github Repo|
|----------------|-------------------------|-----------|-----------|
|DNS|Standard commercial DNS service of AWS||3rd party service|
|SSL Certificate|Standard commercial service of letsencrypt.org||3rd party service|
|Google OAuth Service |Standard commercial serviceof Google||3rd party service|
|t1dpalsys|Installs all other micro-services|||
|host|provides administrative hosting to T1Pal.com containers - Digital Ocean||3rd party service|
|kubernetes|provides kubernetes control;  commercial service of Digital Ocean||3rd party service|
|front|nginx reverse proxy service|||
|t1paldashboard|Provides Content for Web site ||t1paldashboard|
|consul|provides Real Time Configuration Data|||
|landingdb|Patient Database|mongo||
|t1palbackplane|backlib, restify||
|provisioner|Updates multienv|||
|multienv|Nightscout Server |||
|cluster|Kubernetes Control API|||
|backends|Nightscout Proxy|||
|Nightscout|Nightscout|CGM Remote Monitor||
|Helpy Ticketing|Technical Support Processor||3rd party service|
|stripe|Credit Card Transactions|stripe API|3rd party service|
|servicebot.io|Product Management|||
|resolver|Tenant View Resolver|||
|runner|Tenant Runner|||
|dispatcher|Tenant Dispatcher|||
|tenant inspector API|System API|||
|postgres|Application databsse|postgres||


## Responsibilities

1. The CEO and VP-level employees are responsible for overseeing and maintaining this standard operating procedure and for assuring that all employees are trained in its requirements.
2. It is the responsibility of all employees, contractors and departments at Medical Data Networks to adhere to this procedure.
