# Design and Development Controls
Document Number|Title                                      |Effective|Owner
---------------|-------------------------------------------|---------|----
QP-0002        |Design and Development Control Process|9/20/2021|/s/ Ben West

## Purpose

This procedure document defines the controls applicable
to the Design and Development of company products and services.
The company products are all software-based services that run as applications
on commercial cloud hosting providers.

The designs and design artifacts of the delivered applications are also therefore 
all captured and maintained in
software respositories, enabling the company and its customers to benefit
from software-defined service capabilities, where the pathway from
system design to operational realization.

New feature design and development are therefore coupled and completely captured in
github software repositories.   This enables significant automation from
the creation of a proposed feature or service design to a testable and operational software application.

## Scope

This procedure applies to all design and development activities for products intended for commercial distribution.  Applicability of specific phases or deliverables is dependent on the complexity of the product (e.g. product improvement, major modification, or fully designed new product.) 

## Definitions

### **Special Controls**

For FDA Type 2 medical devices, the FDA has outlines **Special Controls** as applicable to these devices.
These are the Special Controls:

Requirement Title|Requirement Text
---------------|-------------------------------------------
REQ_2010 Data Privacy and Modification of Data|All devices sold shall operate in compliance with applicable privacy and modification regulations, including HIPAA
REQ_2020 Protection against modification of data.|All devices shall provide measures to protect against unquthorized access to and modification of data.
REQ_2030 Label A|Device labeling shall display the following warning:  "Dosing decisions should not be made based on this device.  The user should follow instructions on the continuous glucose monitoring system.
REQ_2035 Label B|Device shall include the following limitation:  "This device is not intended to replace self-monitoring practices advised by a physician."

### General Terms and Definitions

* Device History Record (DHR) – Compilation of records containing the production history of a finished device.  
Access to production history for devices may be found in the github repositorie https://github.com/bewest/t1dpalsys  where all design artifacts, software, scripts, and integration specifications are found.

* Device Master Record (DMR) – Compilation of records containing the procedures and specifications for a finished device.  Specifics are contained in 21CRF820.181.  For the purposes of this document, all DMRs are entirely captured by
the company github repository:  https://github.com/bewest/t1dpalsys.

Access to production history for devices may be also found in the collection of github repositories where all software and integration specifications are found.

* Design Input – Physical and performance requirements of a device that are used as a basis for device design

* Design Output – Results of a design effort at each design phase and at the end of the total design effort. The finished design output is the basis for the Device Master Record. The total finished design output consists of the device, its packaging and labeling, and the device master record.

* Design History File (DHF) – Compilation of records containing the design history of a finished device
Access to design history for devices may be found in the collection of github repositories where all software and integration specifications are found.

* Design Review – Documented, comprehensive, systematic examination of a design to evaluate the adequacy of the design requirements, to evaluate the capability of the design to meet these requirements, and to identify problems.

* Design Review Board – a panel of specific named individuals designated to review each phase of each project to make a GO/NO GO decision to advance to the next project phase.

* Validation – Confirmation by examination and provision of objective evidence that the particular requirements for a specific intended use can be consistently fulfilled.

* Risk Management – Systematic application of management policies, procedures, and practices to the tasks of analyzing, evaluating, and controlling risk.

* Master Validation Plan – High level outline of how the design verification, design validation, process validation, and if required, software validation requirements will be met.

* Process Validation – Establishing by objective evidence that a process consistently produces a result or product meeting its predetermined specifications.

* Design Validation – Establishing by objective evidence that device specifications conform to user needs and intended uses.

* Design Verification – Confirmation by examination and provision of objective evidence that specified requirements have been fulfilled.

## Responsibilities

These groups have specific roles in the general process to implement the design and development controls.

* Sales and Marketing – shall have the primary responsibility for determining customer need requirements and developing input specifications, however, all departments are expected to support the development of input requirements and subsequent specifications.

* Operations – is responsible for overseeing the contract manufacturer in executing the transferred design into a salable product, assuring manufacturability and establishing manufacturing requirements. Operations is further responsible for ensuring the creation and maintenance of all DHRs.

* Quality Assurance / Regulatory – has the responsibility of ensuring that product development efforts adhere to Design Control requirements and that all aspects are appropriately documented.  QA is further responsible approval and maintenance / auditing of all DHRs, DMRs, and DHFs.  RA is responsible for regulatory submissions and maintaining compliance to applicable regulatory requirements.

* Product Development/Engineering – has the responsibility for developing and transferring to the Contract Manufacturer a design that is manufacturable and repeatable.  Product Development/Engineering is also responsible for overseeing the development of the DMR, adherence to the Design Control procedures as detailed in this document, responsible for overall project management and for the establishment of project teams and team leaders. 

* Project Leader – is responsible for the project timeline and completion of the deliverables from other departments, for conducting the project team meetings and ensuring that the minutes are taken, issued, and filed, and is responsible for the creation of the Design History File (DHF).

* Equipment and Materials – Equipment and materials vary according to the specifics of each development project.

* Safety Precautions – Use appropriate safety precautions and Personal Protective Equipment required for the processes under development and the equipment that will be used during development.

* Training Requirements – All personnel responsible for completing and/or approving product designs shall be trained to this procedure.

* Record Management – All records associated with the Design Control Process are maintained within the Design History File (DHF) and managed by the Quality Department.
Access to all records as part of the Design Control Process will be found in the collection of github repositories where all software and integration specifications are found.

## Referenced Documents

* 21 CFR 820 FDA – Quality System Regulations

* MDR 2017/745 – EU Medical Device Regulation

* MDD 93/42/EEC – EU Medical Device Directive

* SOR/98-282 – Canadian Medical Device Regulations

* ISO 13485 – Medical Device Quality Management Systems

* ISO 14971 – Medical Devices – Application of Risk Management to Medical Devices

* QF-0002-1 – Design Review Phase Checklist

* QP-0009 – Change Control Process

 
## Design Phase Gate Procedure

The following phase gate system is utilized to control the product design and development process. 

While there may be exceptions and/or further process tailoring, 
this process described as "Design and Development" is applicable
to individual features and/or improvements to the common technology
platform that provides T1Pal services.  

As such, there may be
multiple individual features being developed simultaneously.  The Design and Development process
ends when an electronic version of the Design is tested and pushed into the production lineup.

This github repository contains all of the current system design artifacts:

**https://github.com/bewest/t1dpalsys **

Features of the github service platform (specified elsewhere), are relied on
to provide a definitive history of changes and releases.
The following sequences of processes are used for each and every new feature
and/or bug fix in the system platform.

It should be understood here that the contents of the Github repository
is the system design, and the deployment of proposed updates to the production environment
is fully automated.  All of the automation scripts and software components needed
to deploy the platform are treated as software artifacts, subject to
revision, change control, and release to production.

The following sequence of steps are carried out as needed to define and deploy new features
and/or bug fixes.

### Design Planning:

* Once Executive Management determines that the opportunity is worthy of resources, a Project Team Leader is selected to lead the project and personnel resources from QA/RA, Engineering, Operations, Sales & Marketing and Finance as needed are assigned to form the core project team.  
* The Project Team Leader shall chair individual project team meetings, assigning action items, with completion dates, to the appropriate team members with detailed planning and tracking of tasks. 

* As a guidance and tracking tool, the Project teams will utilize the **Design Review Phase Checklist** to navigate correctly through the phase gated design and development process.

* A **NPD Project Plan/Schedule** shall be developed by the Project Manager and shall include all key project tasks, individual assignments, major milestones such as Phase completion, overall timeline/product launch estimated target, and expected resources.  The NPD Project Plan/Schedule shall be reviewed and updated as necessary at each stage of the phase gate process.  


###  Design Phase Reveiw Meeting Requirement

* Design Phase Review meetings are formal meetings with designated key knowledgeable representatives from a cross section of all disciplines within the company (as applicable to the product), and are intended to update the Leadership Team regarding the project meeting the requirements of the specific phase and gaining approval, or receiving disapproval, to move the project to the next Design Phase.
The **Design Phase Review Checklist** is utilized as the agenda for the phase review meetings and the meeting minutes are recorded.

* At each Design Phase Review, each item for the specific phase must be reviewed on the checklist and where possible the link for each document shall be listed on the checklist.  If an item is not required for a specific product, a brief justification should be listed on the checklist.

* The Design Review Phase Checklist and meeting minutes are the official records of Design Phase Reviews and shall become part of the Product Design History File (DHF).
* At any point in this process the design project may be terminated or suspended as authorized by the Design Review Board.  Reason for termination or suspension shall be recorded in the project Design History File (DHF).

### Phase 1 - Feasibility & Concept

In Phase 1 the project team’s efforts are focused on ensuring that the opportunity makes good business sense by conducting due diligence and completing the following documents to make this determination:

* Customer Needs Document: Developed by Marketing to provide customer analysis and needs, physical appearance, functionality for intended use, any needed user training, and general packaging/labeling requirements for the new product.

* Business Case/Feasibility Study:  Developed by Marketing to summarize the business opportunity, market analysis, how the product will be brought to market, and estimated pricing and project return on investment.

* Design Concept:  Conceptual product representations and configurations, developed by Engineering, intended to meet identified design requirements. 

* Regulatory Strategy:  Completed by QA/RA to determine the product classification and regulatory requirements for FDA, MDD/MDR, CMDR, and all other applicable authorities.  Outline the intended regulatory path for market approval in target markets.

A document entitled **Feasibility & Concept Notes** will capture customer needs, business case, design concept, and regulatory strategy.
This document is maintained on the Google Docs folder for reference and action.

### Phase 2 - Design Inputs and Development

In Phase 2 the project team focuses on further defining the new product concept through development of the following documents: 

* Marketing Launch Plan:  Developed by Marketing describing the launch to market plan in terms of product versions, market segments, time-lines and quantities.

* Manufacturing / Operational Plan:  Developed by Operations describing the overall manufacturing plan from receiving dock door to shipping dock door.  This is typically in the form of a flow chart.  May include imitation of Supplier Qualification, if applicable.

* Packaging & Labeling Requirements:  Developed by Marketing to clearly define the packaging and labeling requirements, including artwork and design patterns.  

* Quality Plan:  Quality developed plan describing how quality will be controlled throughout the design process, project phases, design review meetings, expected outputs to match design inputs, and an outline or description of the overall master validation plan illustrating what verification/validation activities will be performed (e.g. design verification, design validation, process validation and where necessary software validation activities).

* Initial Risk Assessments:  Initial drafts of risk assessments documenting the product/design use, potential risks, and associated mitigating actions.  These assessments are documented within design, process and usability Failure Modes and Effects Analyses (FMEA’s). 

* Initial Traceability Matrix:  Initial drafts of spreadsheet developed by the Project Manager or Engineering linking the required documents throughout the project to the appropriate pre-requisite documents.   At this stage, the spreadsheet should clearly illustrate which design outputs will satisfy specific design inputs.

A Design Input and Verification Checklist will capture all Phase 2 Design Inputs and expected Development Outputs and will be stored in a Google Docs folder.

### Phase 3 - Validation & Verification

In Phase 3 the project team plans and executes verification and validation activities to prepare for design transfer to manufacturing in Phase 4.  The team verifies that the design outputs meet the design input requirements and validates the final design meets the user needs and intended use of the device.  Devices that are intended to be used with other medical devices shall be verified while connected or interfaced.  Design verification and validation shall be conducted on representative product including initial production units, batches, or their equivalents with documented rationale for the selection.

* Design and Usability Risk Assessments:  Team effort led by the Project Leader assessing and documenting the design and usability risks and associated mitigation actions.  These activities are documents in FMEA’s

* Sterilization and Shelf-Life Testing:  Engineering documentation of the verification of the product sterilization and shelf-life requirements.  Sterilization is applicable only if the product is intended to be distributed sterile or able to be sterilized.  

* Biocompatibility Testing: Engineering documentation of the verification of the product biocompatibility requirements.  Standards such as ISO 10993 provide industry accepted testing methodology.  

* Software Validation:  Engineering documentation of the verification of the software design and the validation methods utilized to validate that the software conforms to user needs and intended use.  Applicable only if design incorporates software to achieve functional requirements.  Standards such as IEC 62304 provide methodology.

* Product Safety and Efficacy Testing:  Engineering documentation of the execution of any product safety testing and/or certifications necessary for the release of the device, i.e. IEC 60601-1, IEC 60601-1-2, etc.

* Performance Validation:  Engineering documentation of the verification test methods that will be utilized to verify the performance of the new product design (i.e. precision, accuracy, interference, etc).  

* Usability Validation:  Engineering documentation of the validation methods to be utilized to validate that the design is safe to be used by the intended parties and these parties can effectively use the device.

* Clinical Validation:  Engineering documentation of the validation that the design conforms to user needs and intended use.  May include Clinical Performance Studies, Clinical Evaluation, Clinical Interference Studies, etc.

* Packaging Validation:  Engineering documentation of the validation that the packaging of the product is sufficient to preserve to product during handling, storage and distribution to user and maintain function necessary for intended use.  

* Regulatory Submission:  Actual product submission document (i.e. 510(k), PMA, etc) developed by QA/RA for submission to the appropriate regulatory bodies.

The Design Input and Validation Checklist shall be updted to cover all Phase 3 documentation artifacts.


### Phase 4 - Design Transer to Manufacturing (Commercialization)

In Phase 4 the project team validates that the design and process are correctly translated into production artifacts, Item Masters, BOM’s, Work Instructions and acceptance criteria for the characteristics essential to device functionality.  This phase ensures, that the design is complete, and approved, for meeting the product’s intended use, that the design is documented in the DMR, and is fully placed under change control with a design transfer ECO and completion of the following documents and activities:

The Design and Manufacturing artifacts of this phase are entirely encoded in
scripts, software, control files, and configuration files.   All of these are captured by the github repository 
**https://github.com/bewest/t1dpalsys **

A new "branch" is defined for each new feature package.   The branch is designed, tested, and released to production
under control of the Operations Manager.

* Training:  Operations documentation of the completion of training to all parties responsible for the manufacturing of the final release product.  These include: manufacturing technicians/operators, quality inspectors, final labelers, etc.

* Process FMEA:  Team effort led by the Project Leader assessing and documenting the potential risks of the manufacturing process and associated mitigation activities.

* Process Verification & Validation Plans:  Engineering documentation defining the specific Process Installation, Operational, and Performance Qualification (IQ, OQ, and PQ) requirements for validating the manufacturing equipment and processes, including infrastructure and work environment, prior to release to Manufacturing.  Final reports shall demonstrate that the process has met the pre-defined protocol requirements and produced product that meets pre-defined quality requirements.

* Requirements Traceability Matrix:  A spreadsheet developed by the Project Manager or Engineering linking the required documents throughout the project to the appropriate pre-requisite documents. This spreadsheet should clearly illustrate which outputs will satisfy specific input requirements.

* DMR & DHR:  Final development by the Project Manager of the Device Master Record (DMR) and Device History Record (DHR).  The DMR documents all the validation activities, materials, inspections, processes, etc. that are required to development, manufacture, and release a medical device.  The DHR documents the particular equipment, material(s), documentation, operator(s), etc. that produced a given medical device necessary to maintain traceability and evidence of acceptance.

* Regulatory Approval: Document from the appropriate regulatory bodies providing clearance to market the product.

* Design Transfer ECO: The Project Leader assembles all of the documents required for release to manufacturing into one ECO for approval (e.g. Item Masters, Drawings, BOM’s Work Instructions).

### Phase 5 - Post Market Assessment

This phase typically comes six to twelve months after product market launch and focuses on summarizing and analyzing feedback from the market, and manufacturing, to close the design and development loop and determine if any revisions are required before moving this project formally out of the design and development process.

* Technical File: Comprehensive technical file compiled by QA/RA for CE Marked products.

* Declaration of Conformity: Statement from RA/QA declaring product conformity to the applicable standards and regulations.

* Production Status Report: Document completed by Manufacturing outlining productivity, quality yield conformance to pre-established goals and identifying any open processing issues.

* Customer Feedback: Summary review document completed by QA regarding customer issues and also any customer comments from Marketing.

* Risk Analysis Review:  Final documented review led by the Project Leader to assess overall product risk after six to twelve months in the field. 

* Clinical Evaluation Review:  A documented review led by Project Leader to assess the impacts from the data obtained from the post market surveillance to the clinical evaluation and associated documentation.

### Design Changes

* The company shall identify, document, validate, or where appropriate verify, review, and approve design changes before their implementation.

* The process for design changes after exiting Phase 4 of Design Control is the ECO process.  This process is specified in QP-0009 – Change Control Process.

Proposed, Changed, and bug fixes and features are all captured by at least one branch of the github repository:  https://github.com/bewest/t1dpalsys

Features of the github system provide for tracing, switching to, and testing features and bug fixes.

### Design History File (DHF)

The design history file for products or product families will contain all design activities/documents used to develop the product, accessories, major components, labeling, packaging, and production processes.
Access to the design history file may be found in the collection of github repositories where all software and integration specifications are found.

The design github repository files (DHF) will provide design history for all device features.

The github repository is here:

**https://github.com/bewest/t1dpalsys**

The DHF shall contain or reference the records necessary to demonstrate that the design was developed in accordance with the approved design plan and the requirements of the Quality System Regulation.  DHF records shall be retrievable by analysis of the github commit procedures -- for every feature.

The results of a design review, including identification of the design, the date, and the individuals performing the review, shall be documented in the DHF.

Design verification and validation results, including identification of the design, method(s), the date, and the individual(s) performing the verification and/or validation, shall be documented in the DHF.

### Statistical Calculations

Statistical techniques that are appropriate for the project under development should be used during design and verification.  Rationale for sampling plan selection must be documented.

### Summary of Records

The table of design and development process artifacts below summarizes
the design and development repositories.  These records are expected to be produced by the Design and Development Process.
Please note thta the Github repository for Design and Development artifacts is the 
*t1palsys*  repository.


Record Type|Managed By
--------------------------|
Phase Review Checklist|Google Docs Phase Review Repository Checklist
Design Risk Management Reports|Google Docs Risk Management Reports
Design Verification and Validation Reports |Google Docs Verification and Validation Reports
Design Transfer to Manufacturing|Github repository for Design Artifacts
Design History File (DHF)|Github repository for Design Artifacts

### Revision History

This document  QP-0002_R1_Design_Control_Process.md
is subject to revision. Only the latest approved version should be used.

Major revisions are enumerated below.   
The "latest" and only official version is found in the github document management system governs all QMS activity.

REV #|Doc ID|Effective Date|Description of Change
-----|------|--------------|---------------------
01   | QP-0002|12/17/2014|Initial Release
02   | QP-0002|3/10/2022|Multiple Corrections
02   | QP-0002|3/17/2022|Update for Software Products
02   | QP-0002|3/18/2022|Update for Software github repo updates



