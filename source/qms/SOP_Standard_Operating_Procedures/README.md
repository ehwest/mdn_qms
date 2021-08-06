--- 
folder: "SOP_Standard_Operating_Procedures"
title: "The Quality Management System of Medical Data Networks LLC"
authors:
- github.com/ehwest
approvers:
- github.com/bewest
approval_date: "2020-10-01"
---
# Standard Operating Procedures


```{toctree}
SOP_0001_Control_of_Quality_Records.md
SOP_0002_Employee_Qualification_and_Training.md
SOP_0003_Corrective_and_Preventative_action.md
SOP_0004_Risk_and_Hazard_Management.md
SOP_0005_Complaint_Handling.md
SOP_0006_Medical_Device_Reporting.md
SOP_0007_Access_Controls_to_Software.md
SOP_0008_Gitflow_Tailoring.md
SOP_0009_Semantic_Versioning.md
SOP_0010_Configuration_Management.md
SOP_0011_Performance_Management.md
SOP_0012_Billing_Management.md
SOP_0013_Release_And_Operations_docker-based.md
```

\pagebreak
<center>**Introduction**</center>

This document --together with direct links to other documents-- is a description of the baselined Quality Management System (QMS) that must be followed by all associates of Medical Data Networks LLC (MDN).   

The goal of this QMS is to ensure that company associates and/or work products meet or exeed all of the applicable requirements for planning, manufacturing, validation, certification of Software as Medical Devices provided by 
MDN.  This specific QMS document version is intended to address all of the requirements associated 
with FDA "Class II Medical Devices" realized as software services and operated by MDN.

With this particular release of the QMS, MDN is currently focused on only one "device" named **"T1Pal"**.

T1Pal provides a certified copy of the open-sourced "Nightscout" software 
and operates it on one or more Internet-hosted servers as a service.  Such services are limited to registered subscribers.  In addition, T1Pal offers bundled Technical Support services, and cryptographically-secure remote sharing features not available to other Nightcout software consumers .

While the "open-sourced" Nightscout software has proven to be the popular basis for
"Do It Yourself" (DIY) projects on the Internet, the software installation and operational skills required
makes the Nightscout DIY solution inaccessible to many people.
In addition, the Nightscout software deployed as a DIY project may create unaddressed risks and hazards, including the risk of failures to keep the data private and secure.

Documented US FDA guidelines and requirements have set forth a specific "path" 
for FDA clearance of certain software services (as "medical devices").

It is the intent of this QMS to set forth all of the methods, standards, procedures, etc. as needed
for MDN to realize all of its products and services as FDA "Class II Medical Devices."

The FDA "pathway" for clearance of specific software medical devices has been specifically outlined and --as applied to the present MDN-- is intrepreted  as follows:

1.	MDN must set forth  **"Indications For Use"** of its products and/or services, if any.
2.	MDN must set forth the **"Intended Use"** cases for its products and/or services, 
3.	MDN must provide additional **special controls, validations, and quality controls** aligned with FDA requirements for labeled Intended Use of its products and/or services .

<center>**Table 1 -- List of All T1Pal Intended Use Cases**</center>
Requirement ID | Intended Use Description
---------------|-------------------------
REQ_1010 Secondary Display | It is an intended use for T1Pal to receive data from one or more medical devices and provide a secondary display of the data.
REQ_1020 -- Remote Access | It is an intended use that authorized "followers" will have remote access to a secondary display of the same data.
REQ_1030 -- Technical Support | It is intended that the display of secondary data will be used to provide "Technical Support."  

Note that "Technical Support" in this case is limited to 
providing artifacts, displays, or documentation that hasten:

1. device warranty claims, 
2. guidance on replacement of devices or consumables, and 
3. acts that remedy impairments to data communications.

Under no circumstances should Technical Support be interpreted as providing, correcting, or modifications of medical therapies of any kind.
	
In addition, with the goal of providing "special controls", "validations", and "quality controls" the following additional requirements must be met.

<center>**Table 2 -- Additional T1Pal System Requirementsd** </center>
Requirement ID | Additional Requirements
---------------|------------------------
REQ_2010 -- Data Privacy Protections| The T1Pal is intended to be HIPPA compliant with respect to privacy and access to data.
REQ_2020 -- Protection from modification of data.|The T1Pal is intended to protect against modification of data provided for secondary display.
REQ_2030 -- T1Pal Labelling|The T1Pal software shall provide clear and unambiguous labelling that describes both intended use, and warnings against all other uses.

While certain services of MDN bundle open-sourced components, including Nightscout software,
MDN ensures QMS controls and validation of specific Intended Use labelling, and other privacy and security features outlined above. 

MDN is relying on adherence to this QMS to allow for FDA clearance of MDN products and services
 as a Class II software medical devices that requires no 510(k) submission, and no 513(g) request to commence marketing of the T1Pal product.

MDN products and services are designed, marketed, and specifically limited to "secondary display" of data,
Altogether, the three Intended Use cases, and the Additional System Requirements desceribed below --with the present Quality Management system-- should enable MDN to meet FDA rules for clearance. 

It is the responsibility of all associates, employees, and officers of the company to align their activities with this Quality Management System.  The identification of "Corrective Actions" and follow-on work of company officers will be used to address non-compliance as may be needed to strengthen allignment with this Quality Management System over time.

It should be noted that this Quality Management System is captured in a "github" repository (md_qms) together with a broad range of supporting documents and templates that are expected to be used in the course of business for all Medical Data Networks LLC associates and/or employees and/or contractors.  As such, the instructions are baselined in the "master" branch of this repository and subject to change only by authorized officers of the firm.

It should also be noted that in the event MDN adds products or services other than T1Pal and/or other than certain Class II Medical Devices, this QMS may be changed accordingly.

