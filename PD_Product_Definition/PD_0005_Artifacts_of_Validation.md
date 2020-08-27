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

# Design Verification Review Results

The following table is a work product of the T1Pal Design Review
undertaken 8/27/2020 by Earle West (VP Systems Engineering)  and Ben West (CEO).
This work product is an enumeration of all of the component services
of T1Pal.com, which itself is a micro-service based design.

The function of each and every component in this T1Pal design is completely
captured by its API as shown in the table below.
Each and every API listed has been the target of either automated tests,
code review, and/or manual testing operations.


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


# Product Validation Review Results

Validation of the T1Pal software "device" is routinely the target of one or more tests
of each and every "intended use" as described in the PD_0002_Intended_Use.md document.
Such tests are carried out prior to and during T1Pal operations.

|Requirement|Method of Test|Result|
|-----------------|-------------------------|-------------|
|REQ_1000 Secondary Display|Dynamic with Test Datasets|passed 8/27/2020|
|REQ_1010 Remote Access|Dynamic with Test Datasets|passed 8/27/2020|
|REQ_1020 Documentation Support|Inspection|failed 8/27/2020|
|REQ_1020 Technical Support|Dynamic with Test Datasets|faild 8/27/2020|


## Responsibilities

1. The CEO and VP-level employees are responsible for overseeing and maintaining this standard operating procedure and for assuring that all employees are trained in its requirements.
2. It is the responsibility of all employees, contractors and departments at Medical Data Networks to adhere to this procedure.
