---
repository: "github.com/ehwest/mdn_qms"
folder: "/"
title: "README.md"
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


# Purpose

This document provides a complete overview of the Quality Management System (QMS) used by Medical Data Networks LLC, and in particular, the QMS system used to deliver T1Pal software (...as an FDA device).  

The present Quality Management System (QMS) is specifically designed to achieve and sustain the following goals.

- [ ]  Registration of T1Pal with the FDA
- [ ]  Meet FDA-defined "Special Controls" for T1Pal Operations
- [ ]  Support "Appropriate Validations" for T1Pal as a device
- [ ]  Implement certain "Quality Controls" needed to sustain T1Pal Operations.

In this environment, **"Special Controls"** has been defined by the FDA as follows:

- [ ]  Devices must protect against unauthorized access to and modification of data.

- [ ]  Device labeling must display the following warning: 

  **Dosing decisions should not be made based on this device.**
  
  **The user should follow instructions on the continuous glucose monitoring system.**
  
- [ ]  Device labeling must include the following limitation:  

  **This device is not intended to replace self-monitoring practices advised by a physician.**

While web-site content (and/or any distributed promotional information) for the T1Pal "device" 
is expected to meet all labelling requirements, this QMS is needed to explain
how "protections against unauthorized access to and modification of data is provided by T1Pal.
For this reason, this QMS includes "Product Definition", "Product Development", and "System Design" 
sections needed to convey how this achievement is accomplished and validated.

The order of the folders and files of the QMS system is not intended to convey any particular meaning, except that as a whole, the folders, documents, and their links within this QMS "git" management system capture the complete definition of the QMS.

# Scope

All documents that are a part of the Medical Data Networks LLC "Quality Management System" are "electronic records" as defined in FDA Part 11 regulations for the purposes of access, validation, audit, copying, and record retention.  Any paper, letter, article, or other document relevant to this QMS that is received by Medical Data Networks shall be incorporated into this QMS as an electronic document.

These QMS documents are stored in the private (and secured) root of a "github" repository owned and under control of the CEO of Medical Data Networks LLC. 

As electronic records, they include a collection of organizing electronic folders and individual files that are rendered using "github.com markdown" style of controlling text document display. 

Electronic files that are stored within this repository may have embedded document metadata and markdown symbols that constitute a material part of the controlled document.

Each and every electronic record that is part of the Quality Management System is uniquely named using a string of characters that is the concatenation of the repository root, the folder name under that root, and the file name within that folder.

<repository_root> / <folder_name> / <file_name>

-or-

<repository_root> / <file_name>

By convention, each such component of the whole name has NO SPACES, and used the underscore character "_" to separate memorable elements within the whole string.

Within each document in the system, helpful (but not required) metadata is included within the file identifying the repository root, folder name, and file name. This practice is only intended to facilitate automated assembly and export of Quality Management System documents for casual use. 

Authoritative and controlling Quality Management System documents are available for exraction from the Quality Management System repository, and once they are extracted, the copies should not be considered authoritative and/or controlling. 

Only the repository "master" branch contains authoritative and/or controlling files.  Other branches may be defined for the purposes of review and testing of the QMS system itself.

The git "master" branch of the git repository is the authoritative, approved, operational set of documents that make up the Quality Management System for Medical Data Networks, LLC. 

Individuals may opt to "clone" the entire repository for local off-line reference, and/or may periodically synchronize their own local copy with the controlled "master" branch controlled repository.

A globally unique and immutable electronic "hash" signature computed upon change to any aspect of the Quality Management System is used by the github storage system may be used to determine that a copy of the repository is (and all of the files within it are) identical to the "master" branch of the Quality Management System repository. 

This conveniently enables all consumers of the Quality Management System data procesing tools to determine whether or not they have an exact copy of all of the applicable documents. It also enables convenient read-only access to all incremental changes to any file that is part of the Quality Management System electronic record set. This ensures compliance with FDA Part 11 regulations for audit trail capabilities.

# Folder and File Organization

One or more files are also provided within each  QMS folder, and altogether these folders and files capture the authoritative description of the QMS.  Note that within each of the folders listed below, a special README.md file is included.  The README.md file in each folder is intended to provide an overview of all of the files within the QMS folder.

  + [Standard Operating Procedures (SOP)](https://github.com/ehwest/mdn_qms/tree/master/SOP_Standard_Operating_Procedures)
    + [README.md](https://github.com/ehwest/mdn_qms/blob/master/README.md)
    + [SOP_0001_Control_of_Quality_Records.md](https://github.com/ehwest/mdn_qms/blob/master/SOP_Standard_Operating_Procedures/SOP_0001_Control_of_Quality_Records.md)
    + [SOP_0002_Employee_Qualification_and_Training.md](https://github.com/ehwest/mdn_qms/blob/master/SOP_Standard_Operating_Procedures/SOP_0002_Employee_Qualification_and_Training.md)
    + [SOP_0003_Corrective_and_Preventative_action.md](https://github.com/ehwest/mdn_qms/blob/master/SOP_Standard_Operating_Procedures/SOP_0003_Corrective_and_Preventative_action.md)
    + [SOP_0004_Risk_and_Hazard_Management.md](https://github.com/ehwest/mdn_qms/blob/master/SOP_Standard_Operating_Procedures/SOP_0004_Risk_and_Hazard_Management.md)
    + [SOP_0005_Complaint_Handling.md](https://github.com/ehwest/mdn_qms/blob/master/SOP_Standard_Operating_Procedures/SOP_0005_Complaint_Handling.md)
    + [SOP_0006_Medical_Device_Reporting.md](https://github.com/ehwest/mdn_qms/blob/master/SOP_Standard_Operating_Procedures/SOP_0006_Medical_Device_Reporting.md)
    + [SOP_0007_Access_Controls_to_Software.md](https://github.com/ehwest/mdn_qms/blob/master/SOP_Standard_Operating_Procedures/SOP_0007_Access_Controls_to_Software.md)
    + [SOP_0008_Gitflow_Tailoring.md]( https://github.com/ehwest/mdn_qms/blob/master/SOP_Standard_Operating_Procedures/SOP_0008_Gitflow_Tailoring.md)
    + [SOP_0009_Semantic_Versioning.md](https://github.com/ehwest/mdn_qms/blob/master/SOP_Standard_Operating_Procedures/SOP_0009_Semantic_Versioning.md)
    + [SOP_0010_Configuration_Management.md](https://github.com/ehwest/mdn_qms/blob/master/SOP_Standard_Operating_Procedures/SOP_0010_Configuration_Management.md)
    + [SOP_0011_Performance_Management.md](https://github.com/ehwest/mdn_qms/blob/master/SOP_Standard_Operating_Procedures/SOP_0011_Performance_Management.md)
    + [SOP_0012_Billing_Management.md](https://github.com/ehwest/mdn_qms/blob/master/SOP_Standard_Operating_Procedures/SOP_0012_Billing_Management.md)
    + [SOP_0013_Release_And_Operations_Docker-based.md]( https://github.com/ehwest/mdn_qms/blob/master/SOP_Standard_Operating_Procedures/SOP_0013_Release_And_Operations_docker-based.md)
    + [SOP_0014_Release_And_Operations_k8s-based.md](https://github.com/ehwest/mdn_qms/blob/master/SOP_Standard_Operating_Procedures/SOP_0014_Relase_and_Operations_k8s-based.md)

  + [Communication Materials (CM)](https://github.com/ehwest/mdn_qms/tree/master/CM_Communication_Materials)
    + [README.md](https://github.com/ehwest/mdn_qms/blob/master/CM_Communication_Materials/README.md)
    + [CM_0001_Quality_Manual.md](https://github.com/ehwest/mdn_qms/blob/master/CM_Communication_Materials/CM_0001_Quality_Manual.md)
    + [CM_0002_DEV_OPS_Software_DEV_Process.md](https://github.com/ehwest/mdn_qms/blob/master/CM_Communication_Materials/CM_0002_DEV_OPS_Software_DEV_Process.md) 
    + [CM_0003_Business_Associates_Agreement.md](https://github.com/ehwest/mdn_qms/blob/master/CM_Communication_Materials/CM_0003_Business_Associates_Agreement.md)
    + [CM_0004_Training_Documents.md](https://github.com/ehwest/mdn_qms/blob/master/CM_Communication_Materials/CM_0004_Training_Documents.md)

  + [Product Development Process (PDP)](https://github.com/ehwest/mdn_qms/tree/master/PDP_Product_Development_Process)
    + [REAMDE.md](https://github.com/ehwest/mdn_qms/blob/master/PDP_Product_Development_Process/README.md)
    + [PDP_Phase_1_Research_Select_Changes.md](https://github.com/ehwest/mdn_qms/blob/master/PDP_Product_Development_Process/PDP_phase_1_Research_Select_Changes.md)
    + [PDP_Phase_2_Develop.md](https://github.com/ehwest/mdn_qms/blob/master/PDP_Product_Development_Process/PDP_phase_2_Develop.md)
    + [PDP_Phase_3_Maintenance_Operations.md](https://github.com/ehwest/mdn_qms/blob/master/PDP_Product_Development_Process/PDP_phase_3_Maintenance_Operations.md)
    + [PDP_Phase_4_Release_to_Production.md]( https://github.com/ehwest/mdn_qms/blob/master/PDP_Product_Development_Process/PDP_phase_4_Release_to_Production.md)
    + [PDP_Phase 5_Post_Market_Surveillance.md](https://github.com/ehwest/mdn_qms/blob/master/PDP_Product_Development_Process/PDP_phase_5_Post_Market_Surveillance.md)

  + [Product Definition (PD)](https://github.com/ehwest/mdn_qms/tree/master/PD_Product_Definition)
    + [README.md](https://github.com/ehwest/mdn_qms/blob/master/PD_Product_Definition/README.md)
    + [PD_0001_Product_Environment.md](https://github.com/ehwest/mdn_qms/blob/master/PD_Product_Definition/PD_0001_Product_Environment.md)
    + [PD_0002_Intended_Use.md](https://github.com/ehwest/mdn_qms/blob/master/PD_Product_Definition/PD_0002_Intended_Use.md)
    + [PD_0003_Verification_Methods.md](https://github.com/ehwest/mdn_qms/blob/master/PD_Product_Definition/PD_0003_Verification_Methods.md)
    + [PD_0004_Validation_Methods.md](https://github.com/ehwest/mdn_qms/blob/master/PD_Product_Definition/PD_0004_Validation_Methods.md)
    + [PD_0005_Artifacts_of_Validation.md](https://github.com/ehwest/mdn_qms/blob/master/PD_Product_Definition/PD_0005_Artifacts_of_Validation.md)
    + [PD_0006_HIPPA_Compliance_Statement.md](https://github.com/ehwest/mdn_qms/blob/master/PD_Product_Definition/PD_0006_HIPPA_Compliance_Statement.md)

  + [System Design (SD)](https://github.com/ehwest/mdn_qms/tree/master/SD_System_Design)
    + [README.md](https://github.com/ehwest/mdn_qms/blob/master/SD_System_Design/README.md)
    + [SD_0001_Drawings.md](https://github.com/ehwest/mdn_qms/blob/master/SD_System_Design/SD_0001_Drawings.md)
    + [SD_0002_API_Specifications.md](https://github.com/ehwest/mdn_qms/blob/master/SD_System_Design/SD_0002_API_Specifications.md)
    + [SD_0003_Informative_text.md](https://github.com/ehwest/mdn_qms/blob/master/SD_System_Design/SD_0003_Informative_text.md)

  + [Reference Materials (RM)](https://github.com/ehwest/mdn_qms/tree/master/RM_Reference_Material)
    + [README.md](https://github.com/ehwest/mdn_qms/blob/master/RM_Reference_Materials/README.md)
    + [RM_0001_Government_Identity_Information.md](https://github.com/ehwest/mdn_qms/blob/master/RM_Reference_Materials/RM_0001_Government_Identity_Information)
    + [RM_0002_Security_Audit_Template.md]( https://github.com/ehwest/mdn_qms/blob/master/RM_Reference_Materials/RM_0002_Security_Audit_Template.md)
    + [RM_0003_Security_Privacy_Regulatory_Information.md](https://github.com/ehwest/mdn_qms/blob/master/RM_Reference_Materials/RM_0003.Security_Privacy_Regulatory_Information.md)
    + minutes-pdfjam.pdf

  + [Regulatory Support Artifacts (RSA)](https://github.com/ehwest/mdn_qms/tree/master/RSA_Regulatory_Support_Artifacts)

    + [README.md](https://github.com/ehwest/mdn_qms/blob/master/RSA_Regulatory_Support_Artifacts/README.md)
    + FDA_Petition.md
    + FDA_Policy_for_Device_Software_Functions.pdf
    + Software_as_a_Medical_Device_FDA.pdf

# Change Control

Note that the each and every one of the above folder names and the files within each such folder, and their links to other specific QMS folders within the Quality Management System repository,  altogether completely describe the Medical Data Networks LLC Quality Management System.  

The integrity and traceability of all changes to the Quality Management system is maintained in a "git" repository having its document root located here:  https://github.com/ehwest/mdn_qms. It should be noted that the "master" branch of this repository is the current operational repository of the QMS.  Other branches may be used to draft and test changes to the QMS, but are not further described within the QMS.

As such, all documents and artifacts that are part of the Quality Management System are subject to change-control procedures such that each and every change to the Quality Management System documentation is tracked by explicit versioning enforced by the git repository system.

# License
All documents that are part of the Medical Data Networks LLC repository are either licensed to Medical Data Networks LLC and/or are the private property of Medical Data Networks LLC. 

All documents created or owned by Medical Data Network's employees are considered proprietary trade secrets and are not for disclosure outside of Medical Data Networks LLC, without specific written permission of an officer of Medical Data Networks LLC.


## Responsibilities

1. The CEO and VP-level employees are responsible for overseeing and maintaining this QMS under QMS change-control procedures, and for assuring that all employees are trained in its applicable requirements.
2. It is the responsibility of all employees, contractors and departments at Medical Data Networks to adhere to this QMS.

