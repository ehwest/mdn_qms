
```{toctree}
```

# **Quality Manual Introduction**

Document Number|Title|Effective|Owner
---------------|-------------------------------------|---------|--------
[QM-0001_Quality_Manual_Introduction](./QM-0001_Quality_Manual_Introduction.md)|9/16/2021|/s/ Ben West

**Approvals**

Approving Signature|Name|Role|Date
-------------------|----|----|---
/s/ Ben West       |Ben West|CEO|9/15/2021


## Purpose

This document identified as **QM-0001_Quality_Manual_Introduction**
is one component of the complete Quality Management system (QMS)
used by Medical Data Networks, LLC to enable and operate a
"**Current Good Manufacturing Practices**" as defined
in 21 CFR 820 (an FDA document)..

Other components of the QMS are 
stored, managed, and tracked in this github repository:
https://github.com/ehwest/mdn_qms.

The authoritative list of all components of the QMS system description
 is listed in the index file
./source/index.rst.
This index.rst file may be used by certain repository functions
to automatically generate a formatted easy-to-read PDF file for training and casual use.
(the "make" function 
$ make latexpdf
provides a pdf file with all of the components assembled correctly.
Please note however, that only the repository markdown files are the control files of the repository.
Clones of the repository and/or copies of the PDF file are not controlled.
All files in the repository, including the index.rst file, the make file, and the
markdown files of the QMS components are under change control procedures spelled out
in this document.


## Access
Since this document and all of the components of the Quality Management System Description are stored
in a specific github repository, 
access to the latest and/or any earlier version of any document is readily
available and may be checked out for review by authorized reviewers.   For operational use, the latest version 
approved by any officer of the company (Medical Data Networksm LLC).
should be used.

## Scope

Because the firm products are all entirely operating software applications, 
made to work in a specifically commercially hosted cloud enironment,
we rely on the FDA's characterization of these kinds of applications
as "devices" for which US regulation oversight applies.

In this context, the company does not provide hardware devices or components, only software-defined features and functions.
"Labels" applicable to devices therefore refer to a) labelling on product web sites, b) software application notifications,
c) how-to guides, and d) all other communications by the company.

[FDA Rules](https://www.fda.gov/medical-devices/classify-your-medical-device/class-i-ii-exemptions)
say that all medical devices are subject to the Quality System Regulation (21 CFR 820),
also referred to as the
“Current Good Manufacturing Practices” or “Good Manufacturing Practices,”
unless there is an exception or exemption noted in 21 CFR 820.

This Quality Management System (QMS) is fully 
intended to ensure the compliance of the company and its products
to this and other domestic and international regulations and standards:

* Code of Federal Regulations (CFR), Title 21, Food and Drug
* 21 CFR Part 820 – Quality System Regulation
* ISO 13485 – Medical Devices – Quality Management Systems
* EU Medical Device Regulation – MDR 2017/745
* EU Medical Device Directive – MDD 93/42/EEC
* Other regulatory authorities as appropriate

The contents of a coherent set of files that contain
baselined procedures, templates, and operating records
are strictly managed by change-control procedures, and make this QMS work.

This QMS is made of these types of files.

* Files describing procedures that shall be used by the QMS (QP prefix).
* Files containing templates used by procedures (QF prefix)
* Files Containing filled-in templates (i.e. operational records) (QR-prefix)

Here is a list of all of the components of the 
Medical Data Networks Quality Management System Description.

The Quality Management Systems defined in this manual specifically applies to 
providing "T1Pal"and "CoPilot" cloud-based applications to subscribers, specifically
including the following activities.

* Product Design
* Product Development 
* Network Operations
* Customer Care

By "cloud based" we mean that subscribers are enabled to receive
the benefits of certain operating software applications, but do not maintain, carry, own, or lease  any
particular part of any server, and/or database system necessary to deliver features and functions
of the product.  

Subscribers are required to provide their own
internet (cloud) access arrangements to access the cloud based applications.

In the case of all MDN services,  the subscriber must provide their own  known-working on-line access to
the cloud devices by using a "browser" (or other  mobile application) having an ïnternet connection. The browser
and/or a mobile application
may be configured on any of several types of devices that "act like a modern browser."

In this context, for subscribers to access the "T1Pal"and/or the "CoPilot" features and benefits,
the subscriber must have a qualified device (having a known-compatible version).

This Quality Manual applies to the following facilities where construction, testing, and distribution  of the 
(software) device is carried out.:

*   Medical Data Networks, LLC.,  537 Montridge Ct., Franklin, TN  37067  (Corp HQ / Control)
*   Medical Data Networks, LLC.,  10299 Parkdale Ave, San Diego, CA 92126  (Software Assembly)
*   Medical Data Networks, LLC.,  511 Laurelwood Lane, Charlottsville, VA, 22903  (Operations Management)

The company has undertaken the following roles:
* ISO 13485 – Design, Manufacturer, Contract Manufacturer, Importer.
* US CFR 21 Part 820 – Specification Developer, Manufacturer, Contract Manufacturer, Importer, etc.

The following applicability **exclusions** apply:

* Sterilization Requirement and Processes (ISO Clause 7.5.5 & 7.5.7) – are not provided or distributed sterile products or utilize sterile processes.  

* Implantable Medical Devices (ISO Clause 7.5.9.2 & 8.2.6 Partial) – We do not provide or distribute implantable products.

## Terms and Definitions

Term|Definition
----------------------------------|--------------------------------------------------------------
Appropriate Management|CEO, COO, President, Vice Presidents, Directors, Managers, Team Leaders.
Agile Product Development|A management process, where incrementally-defined demands and solutions are sequentially processed by cross-functional teams and their customers.  With this methodology the initial product is incrementally improved so as to deliver a "Minimum Viable Product (MVP)" having subsequent incremental improvements that are packaged as releases.
Continual improvement|Process of enhancing the Quality Management System to achieve improvements in overall quality, operations, and environmental performance in line with the organization’s Quality Policy.
Controlled Document|Any document that affects the quality of the product and is reviewed and approved prior to release for use or reference.
Corrective Action|A process improvement methodology aimed at identifying and eliminating the causes of known nonconformities and to prevent their recurrence.
Customer|The recipient of a product or service provided by the organization.
Design History File (DHF)|A compilation of records that describes the design history of the finished device.
Device History Record (DHR)|A compilation of records containing the production history of a finished device.
Device Master Record (DMR)|A compilation of records containing the procedures and specifications for a finished device.
Management with Executive Responsibility|Those senior employees who have the authority to establish or make changes to the organization’s quality policy and quality system.
Minimum Viable Product (MVP)|A product version that may be developed and delivered to customers having the least overall cost (and time-to-market) that also acceptably/minimally meets all of the most important customer requirements.
Preventive Action|A process improvement methodology aimed at identifying and eliminating potential causes of nonconformities before they occur.
Process|A set of interrelated resources and activities that transform inputs into outputs.
Process Leader|Person with primary process responsibility to document and maintain its procedures, work instructions, and forms; to control records; and to train process users.   Selected by management based upon primary job responsibilities.
Product|The result of activities or processes.
Proposal|Offer or quote made by an organization in response to a request for a quote to provide product.
Quality Policy|Statement by the organization of its intentions and principles in relation to its overall quality performance which provides a framework for action and for setting the organization’s quality objectives and targets.
Supplier or Vendor|The organization that provides a product or service to an organization.

This QMS includes "Product Definition", "Product Design", "Development", and "Validation"."
sections as needed to convey how cloud-based operating software services (FDA "devices")  "T1Pal" and "CoPilot" are created, delivered, and validated consistent with applicable rules.

The present Quality Management System (QMS) is specifically designed to achieve and sustain the alignment of MDN 
services and/or software "devices" to applicable rules.

The applicable rules are:

1. Registration of T1Pal and CoPilot with the FDA
2. Meet FDA-defined "Special Controls" for T1Pal and CoPilot Operations
3. Support "Appropriate Validations" for T1Pal and CoPilot as "devices".
4. Implement certain "Special Controls" needed to sustain T1Pal Operations.



In this environment, **"Special Controls"** has been defined by the FDA as follows:

    A. Devices must protect against **unauthorized access** to and modification of data.

    B. Device labeling must display the following warnings and limitations: 

        1.  **Dosing decisions should not be made based on this device.**
  
        2.  **The user should follow instructions on the continuous glucose monitoring system.**
  
        3.  **This device is not intended to replace self-monitoring practices advised by a physician.**

It should be noted that the published company "Terms and Conditions", together with other company
website notes are intended to meet all of the labelling requirements.
Further, an active acknowledgement of these Terms and conditions is an enforced 
part of becoming a subscriber to the company "devices".

## Responsibilities

The CEO and VP-level employees are responsible for overseeing and maintaining this QMS under QMS change-control procedures, and for assuring that all employees are trained in its applicable requirements.

The following key processes and interactions define the organizational structure and responsibilities of the Quality Management System.  

```{eval-rst}
.. figure:: ./media/OrganizationChart.png
  :width: 100%
  :name: Organization Chart
  :caption:

```

![Organization Chart](./media/OrganizationChart.png)

These quality system processes are managed in accordance with the requirements of ISO 13485 and applicable regulatory requirements.  Changes to be made to these processes shall be:

* Evaluated for their impact on the quality management system

* Evaluated for their impact on the medical devices produce under this QMS

* Controlled in accordance with the requirements of ISO 13485 and applicable regulatory requirements.

For all outsourced processes that may affect conformance to requirements, the company ensures control over these processes through supplier assessment, purchasing and receiving processes, and/or documented procedures as applicable.  The company maintains responsibility of conformity to applicable international standards and regulatory requirements.  The controls shall be proportionate the risk involved and the ability of the external party to meet the in requirements and include a written quality agreement.

The company has documented procedures for the validation of the application of computer software used in the QMS.  Such software is validated prior to initial use and, as appropriate, after change to the software or its applications.  The specific approach and associated activities shall be proportionate to the risk associated with the use of the software.  Records of such activities are maintained.

All management affected by the controlled documents are responsible to ensure that their personnel are adequately informed and trained, as necessary, to ensure the proper implementation of the procedures. Procedures and records may be created and/or maintained in the form of paper copy, electronic copy, or in other media as deemed appropriate.

The company has established and maintains this document as the Quality Manual. It includes:

* The scope of the quality management system.
* Description and/or definition of procedures established for the quality management system.
* A description of the interactions between the processes of the quality management system.

The company has established and maintains procedures to control all documentation and data related to the requirements of the applicable regulatory standards, including external documents, such as standard and electronic media.  These procedures define the controls for:

* A review and approval process to ensure adequacy and efficacy of documents

* A review process to ensure document content is accurate and updated

* Clear identification and justification of changes

* Ensuring the availability, readability, and accessibility of current documents

* Ensuring documents of external origin, determined necessary, are identified and controlled

* The prevention of deterioration or loss of documents

* The prevention of inadvertent use of obsolete documentation

It is the responsibility of all personnel to keep records of all work or operations performed in the format prescribed by the various policies and procedures in the quality system.  All records shall contain the date of creation and the person responsible for their creation.  All records shall be made in a permanent and legible manner and changes to a record shall remain identifiable.  Controls necessary for the identification, storage, protection, retrieval, retention time, and disposition of records shall be included within the documented procedure requiring the record.  Methods for protecting confidential health information contained in records shall be defined and implemented. 

Management is responsible for establishing a custodian of all quality records, including internal audits, management reviews, corrective actions, preventive actions, training records, proficiency test results, and other related records.  The record retention time is specified by relevant regulatory requirements or documented procedures, whether hard copy or electronic.  

Management demonstrates its commitment to the development and implementation of the Quality Management System, and its continual improvement, by:

* Communicating to the organization the importance of complying with customer, regulatory, and statutory requirements as applicable

* Establishing and communicating the Quality Policy

* Establishing, communicating, and enforcing Quality Objectives

* Conducting management reviews

* Providing necessary resources

Company Management ensures that customer requirements and applicable regulatory requirements (needs and expectations) are understood and are met with the aim of enhancing customer satisfaction.  These are generally established within product requirements and specifications and within quality management system documentation.

The *Quality Policy* is established by management with executive responsibility.  The company quality policy is stated below and is communicated throughout the organization to ensure commitment to quality within the organization.  The quality policy provides a framework for establishing and reviewing quality objectives and is reviewed periodically for continued effectiveness.


**Every employee accepts responsibility for the quality of our processes and medical devices.** 

This is achieved by continuously improving designs, implementing efficient procedures, and partnering with suppliers to meet or exceed the expectations of our customers, and satisfy the requirements of our quality system and appropriate regulations.

For each medical device type or medical device family, we have established and maintain one or more files containing or referencing documents generated to demonstrate conformity to the requirement of ISO 13485 and applicable regulatory requirements.  The content of the file(s) includes:

* General description of the medical device, intended use/purpose, and labeling, including any instructions for use

* Specifications for the product

* Specifications or procedure for manufacturing, packaging, storage, handling, and distribution

* Procedures for measuring and monitoring

The company has identified the following Quality Objectives.  These objectives will be reviewed and updated as necessary to meet company goals.

* Establish and maintain a team-oriented working environment in which each employee accepts responsibility for the development, production, and delivery of high quality goods and services.

* Implement and maintain a Quality System compliant with the Quality System Requirements of the United States Food and Drug Administration (FDA), ISO 13485, European Union, and any other applicable regulatory requirements.

* Implement and maintain efficient quality systems and procedures that effectively control the quality of the products and services provided and emphasize continuous improvement.

* Define and monitor metrics of effectiveness for key elements of the business and utilize the data to effectively manage and drive improvement with emphasis on Customers, Products, Services, and Stakeholders.


Management ensures that the planning of the Quality Management System is implemented by appropriate management and carried out by all employees in order to meet the requirements provided in this manual. Management also ensures the integrity of the Quality Management System is maintained when changes to the Quality Management System are planned and implemented.  

Management has defined and documented the responsibility, authority, and interrelation of personnel who manage, perform, and verify work within the Quality Management System.  These responsibilities are documented in official job descriptions, which define the tasks performed by employees, and an organization chart depicting the interrelation of all employees.

All employees accept responsibility for the maintenance and improvement of the Quality Management System.  

This is achieved by understanding and supporting the Quality Policy and the appropriate clauses of the quality system for their areas of work; 
dedicating efforts to the continuous improvement, understanding how their activities impact quality, elimination and prevention of quality deficiencies; 
and initiating action to prevent the occurrence of nonconformities related to product and processes.

The Management Representative is appointed by management with executive responsibility and is responsible and fully authorized to manage the Quality Management System and related matters on an ongoing basis.  Roles and responsibilities of the Management Representative include the following:

* Ensures that the Quality Management System is established, implemented, and maintained in accordance with applicable regulatory requirements.

* Interprets applicable standards and continually verifies compliance.

* Advises management regarding operation and performance of the quality systems and opportunities for improvement.

* Serves as liaison to external parties regarding matters relating to the QMS.

* Ensures the promotion of awareness of applicable regulatory, quality management, and customer requirements throughout the organization.

The Management Representative has the responsibility to work with other departments to ensure that adequate internal communication exists concerning the effectiveness and implementation of the Quality Management System.

Methods for internal communication include:

* Meetings

* Memos

* E-mails

* Formal Training

Management acknowledges responsibility for the quality systems and reviews the systems to ensure continuous suitability and effectiveness in relation to domestic and international regulatory requirement, this Quality Manual, and company objectives.  Management representing each key functional area participates in this review that includes assessing opportunities for improvement and the need to change the Quality Management System, including the Quality Policy and Objectives.  Records of management reviews are maintained.

The activities reviewed during management reviews may include, but are not limited to:

* Feedback
* Customer complaint handling and trending
* Reporting to regulatory authorities
* Internal or third-party audits
* Monitoring and measurement of processes and products
* Corrective and preventive actions
* Previous management review activities
* Changes that could affect the Quality Management System
* New or revised regulatory requirements

The output from management review meetings may include decisions and actions relating to:

* Improvement needed to maintain the suitability, adequacy, and effectiveness of the Quality Management System and its procedures
* Improvement of the product, services, training, infrastructure, work environment, and other processes
* Changes needed to respond to applicable new or revised regulatory requirements
* Resource requirements and allocation

Management has the responsibility and authority to ensure there are adequate resources to support the Quality System throughout their functional areas of responsibility.  Each member of management is to provide adequate resources to:

* Implement and maintain the Quality Management System and continually improve its effectiveness
* Enhance customer satisfaction by meeting customer requirements
* Meet regulatory requirements
* Place trained and competent personnel in the right place at the right time to ensure company goals and objectives are met

Resource and training requirement are identified and addressed on a regular basis in order to support the growth and changing needs of the company.  For each job function, management provides sufficient personnel with appropriate background, education, and experience.

The company has established and maintains documented procedures for establishing competence, providing needed training, and ensuring awareness of personnel.  These procedures include:

* Determining the necessary competence of personnel performing work affecting quality
* Providing training or other actions to achieve or maintain the necessary competence
* Evaluation of the effectiveness of the training and other actions taken.  The methodology for effectiveness check is proportionate to the risk associated
* Ensuring that personnel are aware of the importance of their activities and how they contribute to the achievement of quality objectives
* Maintaining appropriate records of education, training, skills, and experience.

Management maintains responsibility for infrastructure needed to produce quality products and services and documented the requirements for the work environment needed to achieve conformity to product requirements, prevent product mix-up, and ensure orderly handling product.  Infrastructure includes:

* Buildings, workspace, and associated utilities

* Process equipment (both hardware and software) 

* Supporting services (i.e. transport, communication, or information systems)

This infrastructure is reviewed and adjusted as needed to achieve company objectives.  

A documented procedure shall be established for any infrastructure maintenance activities, including interval of performing the maintenance activities when required, necessary to maintain quality and records of such activities shall be maintained. As appropriate, the requirements shall apply to equipment used in production the control of work environment, and monitoring and measurement.

The company maintains responsibility and has documented the requirements for the work environment to assure its suitability for achieving conformity to product requirements.

Where appropriate to ensure quality and compliance with applicable Environmental, Health, and Safety (EHS) requirements, the company has established:

* Documented requirements for health, cleanliness and clothing of personnel if contact between such personnel and the product or work environment could affect medical device safety or performance
* Documented requirements for environmental conditions and instructions for monitoring and controlling these conditions
* Training for personnel working temporarily under special environmental conditions

As appropriate, the organization has planned and documented arrangements for the control of contamination or potentially contaminated product in order to prevent contamination of the work environment, personnel, or product

The quality planning requirements for individual development projects, related processes and supporting documentation are described in the procedures for each of several well-defined process, for example, the design control procedure, supplier qualification procedure and other process procedures.  The company has developed a documented risk management procedure and maintains records of risk management activities.


The quality planning process, when initiated, shall provide for the following:

* Identification and acquisition of necessary controls, equipment, fixtures, resources and skills needed to achieve business goals and objectives.

* Provision for procedures, work instructions, inspections, tests, etc. to ensure product is manufactured to customer expectations and requirements including infrastructure and work environment.

* Required verification, validation, monitoring, measurement, inspection, test, handling, storage, distribution, and traceability activities specific to the product together with the criteria for product acceptance.

* Records needed to provide evidence that the realization processes and resulting product meet requirements.

The company has established and maintains a process for identifying hazards associated with products and processes, estimating and evaluating the associated risks, controlling these risks and monitoring the effectiveness of the control including post-production information. Documented risk management activities are included throughout the product realization process, where appropriate.  Records arising from risk management are maintained in a risk management file.

The determination of the requirements relating to the product includes:

* Requirements specified by the customer including delivery, service and support, and product performance
* Requirements not specified by the customer but necessary for intended use, where known
* Statutory and regulatory requirements relating to the product
* Any user training needed to ensure specified performance and safe use of the product
* Additional requirements determined by the organization

Contracts, including purchase orders, are reviewed to ensure customer requirements and amendments are communicated in a controlled manner.  The contract review requires the appropriate review of each proposal, contract, or order to ensure that:

* Product requirements are defined and documented
* Contract or order requirements differing from those previously expressed are resolved
* Applicable regulatory requirements are met
* Any user training identified in accordance with 7.2.1 is available or planned to be available
* The organization has the ability to meet the defined requirements

Amendments to a contract or customer’s specification are handled and correctly transferred to the concerned functions within the company and confirmed with the customer.

All management affected by the controlled documents are responsible to
ensure that their personnel are adequately informed and trained, as
necessary, to ensure the proper implementation of the procedures.
Procedures and records may be created and/or maintained in the form of
paper copy, electronic copy, or in other media as deemed appropriate.

Records of contracts, contract reviews, proposals and contract amendments are maintained in the customer file.

The company plans and documents effective arrangements for communicating with customers in relation to:

* Product information
* Inquiries, contracts, and order handling, including amendments
* Customer feedback, including customer complaints, and customer satisfaction
* Advisory notices
We have documented procedures for communicating with regulatory authorities in accordance with applicable regulatory requirements

Documented procedures shall be used to control and verify the development of new products to ensure that the specified requirements are met.  

All of the products of MDN are currently defined entirely by software. In addition,
all of the supporting integrated services, data structures, and infrastructure component services are also
defined by software, and managed using configuration files.

Supporting this all-software approach to developing products, an "agile" process that implements "continuous integration"  and "çontinuous delivery" has been established
for all products developed by MDN.  

It should be noted that the goal of the original product release was to deliver
a "Minimum Viable Product (MVP)" that represents a minimal set of features that all meet the customer expectations and requirements (including any regulatory requirements).

Following the delivery of the MVP, subsequent small (i.e. agile) releases would be expected to rapidly deliver new and improved capabilities (i.e. "as if" the process were continuous).

Design input requirements relating to the product are identified, documented, and reviewed for adequacy.  Design input requirements include:

* Functional, performance, usability, and safety requirements, according to its intended use

* Applicable statutory and regulatory requirements and standards

* Applicable output(s) of risk management

* As appropriate, information derived from previous similar designs

* Other requirements essential for design and development of the product and processes

Design input requirements are reviewed for adequacy and incomplete, ambiguous, or conflicting requirements are resolved.  Requirements shall be complete, unambiguous, able to be verified or validated, and not in conflict with each other.

Design outputs are provided in a form suitable for verification against design input and are approved prior to release.  Design outputs:

* Demonstrate that input requirements have been met

* Provide appropriate information for purchasing and production

* Contain or reference product acceptance criteria

* Specify product characteristics essential for its safe and proper use

The design control procedure requires that systematic design and development reviews be conducted to:

* Evaluate the ability of the design to meet the requirements

* Provide for a review by participants representing concerned functions as well as other specialized personnel

* Identify any deficiencies and propose necessary actions 

Participants in these reviews include representative from relevant functional areas and specialist personnel, concerned with the design stage being reviewed.

Records of the results of design reviews and any necessary actions are maintained and include the identification of the design under review, the participants involved and the date of the review.

It is the responsibility of all personnel to keep records of all work
or operations performed in the format prescribed by the various
policies and procedures in the quality system. All records shall
contain the date of creation and the person responsible for their
creation. All records shall be made in a permanent and legible manner
and changes to a record shall remain identifiable. Controls necessary
for the identification, storage, protection, retrieval, retention
time, and disposition of records shall be included within the
documented procedure requiring the record. Methods for protecting
confidential health information contained in records shall be defined
and implemented.

Management is responsible for establishing a custodian of all quality
records, including internal audits, management reviews, corrective
actions, preventive actions, training records, proficiency test
results, and other related records. The record retention time is
specified by relevant regulatory requirements or documented
 procedures, whether hard copy or electronic.

Design and development verification is performed in accordance with planned and documented arrangements to ensure that design outputs comply with design input requirements.
The company documents verification plans that include methods, acceptance criteria and, as appropriate, statistical techniques with rational for sample size.

If the intended use requires that the medical device be connected to, or have an interface with, other medical device(s), verification shall include confirmation that the design outputs meet design inputs when so connected or interfaced.

Management demonstrates its commitment to the development and
implementation of the Quality Management System, and its continual
improvement, by:

* Communicating to the organization the importance of complying with customer, regulatory, and statutory requirements as applicable

* Creating records of the results and conclusions of design verification and any necessary actions.

Design validation is performed in accordance with planned and documented arrangements to ensure that the design is capable of meeting the requirements for the specified application or intended use, where known.  

The company documents validation plans that include methods, acceptance criteria and, as appropriate, statistical techniques with rationale for sample size.

As part of design and development validation, the organization shall perform clinical evaluation or performance evaluations of the medical device in accordance with applicable regulatory requirements.  A medical used for clinical evaluation or performance evaluation is not considered to be released for use to the customer.

If the intended use requirement that the medical device be connected to, or have an interface with, other medical device(s), validation shall include confirmation that the requirements for the specified application or intended use have been met when so connected or interfaced.

Validation will be performed prior to the release for use of the product to the customer

Records of the results and conclusions of design validation and any necessary actions are maintained.

Design transfer is performed in accordance with planned and documented arrangements to ensure the transfer of design and development outputs to manufacturing.  These procedures ensure that design and development outputs are verified as suitable for manufacturing before becoming final production specification and that production capability can meet production requirements.

Records and conclusions of the results of design validation and any necessary actions are maintained.

Design changes and modifications are identified, documented, reviewed, and approved by appropriate management prior to implementation.  The company determines the significance of the change to function, performance, usability, safety, and applicable regulatory requirements for the medical device and its intended use.

Design and development changes are identified and before implementation, the changes are reviewed, verified, validated (as appropriate), approved.

The review of design and development changes shall include evaluation of the effect of the changes on constituent parts and product in process or already delivered, inputs or outputs of risk management, and product realization processes.

The company has identified the following Quality Objectives. These
objectives will be reviewed and updated as necessary to meet company
goals.

-   Establish and maintain a team-oriented working environment in which
    each employee accepts responsibility for the development,
    production, and delivery of high quality goods and services.

-   Implement and maintain a Quality System compliant with the Quality
    System Requirements of the United States Food and Drug
    Administration (FDA), ISO 13485, European Union, and any other
    applicable regulatory requirements.

-   Implement and maintain efficient quality systems and procedures that
    effectively control the quality of the products and services
    provided and emphasize continuous improvement.

-   Define and monitor metrics of effectiveness for key elements of the
    business and utilize the data to effectively manage and drive
    improvement with emphasis on Customers, Products, Services, and
    Stakeholders.

The company maintains a design and development file for each medical device type or medical device family.  This file includes or references records generated to demonstrate conformity to the requirements for design and development and records for design and development changes.

The company plans and implements the monitoring, measurement, analysis, and improvement processes needed to:

* Demonstrate conformity of the product
* Ensure conformity of the Quality Management System
* Maintain and continually improve the effectiveness of the product
* Maintain and continually improve the effectiveness of the QMS

As one of the measurements of the effectiveness of the quality management system, the company gathers and monitors information relating to whether the organization has met customer requirements.  The methods for obtaining and using this information are documented.  This feedback process includes provisions to gather data from production as well as post-production activities.

The information gathered in the feedback process serves as potential input into risk management for monitoring and maintaining the product requirements as well as the product realization or improvement processes.

If applicable regulatory requirements require us to gain specific experience from post-production activities, the review of this experience shall form part of the feedback process.

The company has implemented documented procedures for timely complaint handling in accordance with applicable regulatory requirements.

These procedures include at a minimum requirements and responsibilities for:

* Receiving and recording information
* Evaluating information to determine if the feedback constitutes a complaint
* Investigating Complaints
* Determining the need to report the information to the appropriate regulatory authorities
* Handling of complaint-related product
* Determining the need to initiate corrections or corrective actions


If any complaint is not investigated, justification shall be documented.  Any correction or corrective action resulting from the complaint handling process shall be documented.

If an investigation determines activities outside the organization contributed to the complaint, relevant information shall be exchanged between the organization and the external party involved.

Complaint handling records are maintained.


## Quality System Quick Access Facility

This section informally enumerates each of the Quality Procedures used to operate Medical Data Networks, LLC so as to deliver quality products that align with applicable rules and regulations.
The controlled version of this is managed by the ./source/index.rst file within the QMS repository.

In addition the table below provides information on the "Record-Keeping Template(s)" which is information
that is formally controlled by identifying the template within the procedure description.


**Quality System Procedures**

| **Document ID**| **Procedure**  | **Record-Keeping Template(s)** 
|----------------|----------------|-----------------
|                |                |             
|[QP-0001 R1](QM-0001_Quality_Manual_Introduction.md) (this document)|Quality Manual Update Process|N/A
|[QP-0002 R1](./QP-0002_Design_Control_Process.md)|Design Control Process|[QF-0002 Design_Control_Records](./Design_Control/README.md)
|[QP-0003 R1](./QP-0003_Document_Control_Process.md)|Document Control Process|N/A
|[QP-0004 R1](./QP-0004_Training_and_Competency_Process.md)|Training and Competency Process|[QF-0004 Training and Competency Records](./Training_and_Competency_Records/README.md)
|[QP-0005 R1](./QP-0005_Purchasing_and_Receiving_Process.md)|Purchasing and Receiving Process |[QF-0005 Purchasing Controls](./Training_and_Competency_Records/README.md)|N/A
|[QP-0006 R1](./QP-0006_Labeling_and_Packaging_Control_Process.md)|Labeling and packaging Control|N/A
|[QP-0007 R1](./QP-0007_Identification_and_Traceability_Process.md)|[Traceability Records](./Traceability_Records/README.md)|Not defined yet 
|[QP-0008 R1](./QP-0008_Nonconforming_Product_Process.md)|Nonconforming Product process|[QF-0008 Non Conforming Product](./Non_conforming_Product.md)
|[QP-0009 R1](./QP-0009_Change_Control_Process.md)| Change Control Process
|[QP-0010 R1](./QP-0010_Software_Development_and_Validation_Process.md)| Software Validation Process
|[QP-0011 R1](./QP-0011_Customer_Complaint_Handling_Procedure.md)| Customer Complaint Handling Procedure|[QF-0011 Customer Complaints](./Customer_Complaints/README.md)
|[QP-0012 R1](./QP-0012_Corrective_and_Preventive_Action_CAPA_Process.md)|Corrective and Preventive Action|[QF-0012 CAPA Forms](./Corrective_and_Preventive_Action./README.md)
|[QP-0013 R1](./QP-0013_Management_Review_and_Data_Analysis_Process.md)|Management Review and Data Analysis Process|[QF-0013 Management Review](./Management_Review/README.md)Not defined yet
|[QP-0014 R1](./QP-0014_Calibration_and_Preventive_Maintenance_Process.md)|Calibration and Preventive Maintenance Process|[QF-0014 Calibration and Preventive Maintenance Process](./Calibration_and_Preventive_Maintenance/README.md)|Not defined yet
|[QP-0015 R1](./QP-0015_Quality_Audit_Process.md)|Quality Audit Process|[QF-0015 Internal Audit Records](./Internal_Audits/README.md)| Not defined yet           
|[QP-0016 R1](./QP-0016_Preservation_of_Product_Process.md)                 | Preservation of Product Process|N/A
|[QP-0017 R1](./QP-0017_Risk_Management_Process.md)| Risk Management Process|
|[QP-0018 R1](./QP-0018_Record_Management_Process.md)| Record Management Process|N/A
|[QP-0019 R1](./QP-0019_Customer_Property_Control_Process.md)| Customer Property Control Process|N/A
|[QP-0020 R1](./QP-0020_FDA_Audit_Management_Process.md)| FDA Audit Management Process|N/A|Not defined yet
|[QP-0021 R1](./QP-0021_Medical_Device_Reporting_and_Recall_Process.md)|Medical Device Reporting and Recall Process|[QF0021 Medical Device Reporting and Recall Records](./Medical_Device_Reporting_and_Recall/README.md)|Not defined yet
|[QP-0022 R1](./QP-0022_Infrastructure_and_Work_Environment.md)|Infrastructure and Work Environment|N/A|Not defined yet
|[QP-0023 R1](./QP-0023_Supplier_Management_Process.md)|Supplier Management Process|Not defined yet
|[QP-0024 R1](./QP-0024_Post_Market_Surveillance_Process.md)|Post Market Surveillance Process|[QF-0024 Post Market Surveillance](./Post-Market_Surveillance/README.md)| Not defined yet
|[QP-0025 R1](./QP-0025_Unique_Device_Identification_Process.md)|Unique Device Identification Process|| Not defined yet
|[QP-0026 R1](./QP-0026_Process_Validation_Procedure.md)|Process Validation Procedure|N/A| Not defined yet|
|[QP-0027 R1](./QP-0027_Technical_File_Process.md)|Technical File Process|N/A| Not defined yet
|[QP-0028 R1](QP-0028_European Union Medical Device Directive Procedure.md)| European Union Medical Device Directive Procedure|| Not defined yet
|[QP-0029 R1](QP-0029_European_Union_Medical_Device_Regulation_Procedure.md)| European_Union_Medical_Device_Regulation_Procedure|| Not defined yet
|[QP-0030 R1](QP-0030_Canadian Medical Device Regulations Procedure.md)| Canadian Medical Device Regulations Procedure|N/A | Not defined yet



## License

All documents that are part of the Medical Data Networks LLC repository are either licensed to Medical Data Networks LLC and/or are the private property of Medical Data Networks LLC.

All documents created or owned by Medical Data Network's employees are considered proprietary trade secrets and are not for disclosure outside of Medical Data Networks LLC, without specific written permission of an officer of Medical Data Networks LLC.


## Revision History

This Quality Manual is subject to change.

Major revisions are enumerated below.   
Because the git repository for all QMS documents is github and github provides by default the latest
official version,  version tracking is built into the system.
By downloading a copy of the Quality Manual and and/or any of the procedures, you are guaranteed to have the latest version.

REV #|Doc ID|Effective Date|Description of Change
-----|------|--------------|---------------------
01   |Quality Manual| 9/15/2021|Initial Release of the Quality Manual
02   |QM-0001_Quality_Manual_Introduction|3/11/2022|Markdown Corrections
02   |QM-0001_Quality_Manual_Introduction|3/17/2022|Details on QMS Records Added


