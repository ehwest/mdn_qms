---
repository: "github.com/ehwest/mdn_qms"
folder: "/"
title: "REAMDE.md"
document_id: ""
authors:
- github.com/ehwest
approvers:
- github.com/bewest
revision: "05"
approval_date: "2020-08-24"
effective_date: "2020-08-24"
description: "Medical Data networks Quality Management System"
---


## Purpose

This document provides an overview of each element of the Quality Management system used by Medical Data Networks LLC, and in particular, the system supporting the T1Pal software product.

The Quality Management System includes these parts:

# Standard Operating Procedures (SOP).
## Control of Quality Records
## Employee Qualification and Training
## Corrective and Preventative Action
## Risk and Hazard Management
## Compliaint Handling
## Medical Device Reporting
## Getting access to the software and component services.
## Gitflow tailoring used for T1Pal
## Semantic Versioning
## Configuration Management
## Performance Management
## Billing Management
## Release and Operations Process (docker-compose version)
## Release and Operations process (K8s version)

# Communication Materials (CM)
## Quality Manual
## Overall DEV/OPS Software Development Process 
## Business Associates Agreement
## Training Documents

# T1Pal Product Definition (PD)
## Product Requirements
## Intended Use
## Verification Methods
## Validation Methods
## Artifacts of Validation
## HIPAA Compliance Statement (how we comply)

# Product Development Process (PDP)
## Phase 1 -- Research select changes
+ Developer gets requirements for the change to be made.
## Phase 2 -- Develop
+ Cut a new feature branch for that change
+ Do development on that branch
+ When ready, developer puts it on shared developer branch (DEV)
+ Automated testing happens automatically
+ Reviewers sign off on changes
+ Components go to master branch (refer to gitflow)
+ Cut a new release for a new version (refer to semantic versioning)
## Phase 3 -- Maintenance Operations
+ Fault Management
+ Perform Backups of the current system
+ system health check
+ validate events
+ fix or roll back
## Phase 4 -- Release changes to production
+ Go through a release process to deploy code on servers
+ refer to SOP for release
+ update SOP as needed
## Phase 5 -- Post Market Surveillance
+ identification of new features
+ identify and triage operations bug fixes

# Reference Materials (RM)
## Government Identity Information
## Security Audit Template
## Security Privacy Regulatory Information

# Regulatory Support Artifacts (RSA)
## FDA Piolicy for Device Software Functions
## IMDRF_TECH_151002_sAMD-QMS.pdf
## Software As A Medical Device.
## Guidance for Industry (part 11, Electronic Records)
## 21 CFR part 11 Compliance Checklist

# Representative Artifacts of the System Design (SD)
## Drawings -- including System Architecture and Design
## API Specifications
## Informative Text

## PHASE 3

## Phase 2 -- 

## Responsibilities

1. The CEO and VP-level employees are responsible for overseeing and maintaining this standard operating procedure and for assuring that all employees are trained in its requirements.
2. It is the responsibility of all employees, contractors and departments at Medical Data Networks to adhere to this procedure.
