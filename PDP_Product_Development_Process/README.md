---
repository: "github.com/ehwest/mdn_qms"
folder: "PDP"
title: "README.md"
document_id: ""
authors:
- github.com/ehwest
approvers:
- github.com/bewest
revision: "05"
approval_date: "2020-08-24"
effective_date: "2020-08-24"
description: "(PDP) Product Development Process"
---


## Purpose

This file contains an overview of the Medical Data Networks LLC Product Development Process.

The Product Development Process is by definition the process by which changes to software and services that are used in the T1Pal application and its supporting infrastructure.

The complete Product Developmetn Process is composed of 5 phases.
+ Phase 1:  Research and select specific changes to Standard Operating Procedures to capture in a modified system design.  The deliverable for this phase is the requirements for the change to be made.
+ Phase 2: Develop Software changes by modifying, deleteing, and/or adding code.  There are 6 steps in this phase:
    +  Cut a new feature branch for the change and do development on that feature branch.
    +  When ready, the developer puts the code on a shared developer branch (DEV) for team review and automated testing.
    +  Automated testing happens, triggered by placement of developed code onto the DEV branch.
    +  Technical reviewers sign-off on changes based on test findings.
    +  Changed software is pushed to master branch (per gitflow process)
    +  Cut a new software relase to production using semantic versioning.

+ Phase 3: Maintenance Operations
    +  Review and adjust Fault Management solution (health checks)
    +  perform backups of any impacted dataset.
    +  perform system health checks
    +  validate events detected
    +  fix or roll back software

+ Phase 4:  Release changes to production
    +  follow the release process to deploy code.
    +  if needed, update the SOP
    +  if needed, update the support knowledge base.

+ Phase 5:  Post Market Surveillance
    +  address all of the outstanding bugs reported and assess relative value
    +  address "pain-points" of current and prospective users.
    +  address the features needed to enter new, adjacent markets
    +  address features in the value chain (above and below) to address cost reductions and performance improvements.


## Responsibilities

1. The CEO and VP-level employees are responsible for overseeing and maintaining this standard operating procedure and for assuring that all employees are trained in its requirements.
2. It is the responsibility of all employees, contractors and departments at Medical Data Networks to adhere to this procedure.
