---
repository: "github.com/ehwest/mdn_qms"
folder: "SOP_Standard_Operating_Procedures"
authors:
- github.com/ehwest
approvers:
- github.com/bewest
approval_date: "2020-10-01"
---

\pagebreak
# Design, Release and Operations Management

**T1Pal Code Repository and the Gitflow Process**

It is the standard procedure to use github.com as a service provider for software.
In addition, it is the standard procedure to follow the "Gitflow" method for
managing improvements to software targeted for the T1Pal platform.
Gitflow as tailored to meet T1Pal requirements is further described in Chapter 13 [QMS SOP_0008_Gitflow_Tailoring.md](https://github.com/ehwest/mdn_qms/blob/master/SOP_Standard_Operating_Procedures/SOP_0008_Gitflow_Tailoring.md) 
section of this QMS system.

Any and all software released as part of T1Pal shall first be introduced to (i.e. created on) the T1Pal platform
as a branch of the T1Pal github code repository.  All software is created first on either of the following
two branches:  

1. <named> "**feature**" branch -- for software not yet associated with a relase.
2. "**development**" branch -- for software definitely targeted to a particular relase.


Following the "**gitflow**" process, all T1Pal "code" goes into this github code repository.   
By "code" we include the following artifacts:

* software of any particular language (javascript, Ruby, PHP, BASH)
* configuration files (e.g. nginx, apache web server configuration files)
* service definition files (e.g. docker files, .yaml files for Kubernetes, HOLM charts)
* Instructions for manually configuring services from a particular platform service provider (e.g. Digital Ocean servers, AWS, MongoDB, Redis, postgresdb)

Component services built on Docker containers shall be "built" using Docker files controled by 1) a docker command-line or 2) a script.

In either case, the command-line and/or the script shall itself be included in the development github repository.
Configuration parameters for all functions of a docker container shall be provided within the Docker file, and stored in the github repository.

A specific BASH script shall be used to trigger the transfer and activation of new product instances.

T1Pal uses a number of external services that are configured manually and then operationally accessed using a well-defined
API.  These including stripe.com, servicebot.io, MongoDB, postgresdb, DNS, Kubernetes clusters, and Digital Ocean hosting services.
It is the goal of T1Pal to leverage all such public services to the maximum extent possible, subject
to operational cost, reliability, security, and performance requirements.

Step-by-step procedures to manually create and utilize any external service shall be documented in the T1Pal development github repository in .md format.

**Release Process**
A "release" of new or changed software to production amounts to promoting the "staging" branch of the github repository to the "master" branch of the github repository, where it can be tested prior to final release.

The production branch of the repository "should" exactly match the deployed production software.

The release process generally involves logging into a production server so as to remotely "check out" the correct development branch from the github repository.
Each component of the T1Pal system has it's own "repo" that has a development, staging, feature, and release branches.   

The "staging" branch of the github repository contains the tested final version to be promoted to production.   The "staging" branch is subject to extensive testing and is only available to operations staff.

A "run-book" is a check-list style document (stored in the github repository) that provides all of the methods and procedures needed to promote a "staging" branch to the "production" branch and test for correct operation.   Testing of the run-book is also done in the staging environment.

Prior to checking out the production software on a T1Pal component (from the master repo), a data transition script may be required to prepare the production environment with the right data, in the right schema.  A backup of the production data must be done for all software changes impacting data.

## General Design and Development Planning Processes

It is the policy of T1Pal to align with "FDA 21 CFR 820.30 (b)"  with respect to design and development planning:

"Each manufacturer shall establish and maintain plans that describe or reference the design and development activities and define responsibility for implementation. 

The plans shall identify and describe the interfaces with different groups or activities that provide, or result in, input to the design and development process. 

The plans shall be reviewed, updated, and approved as design and development evolves."

MDN uses an iterative, agile development process. Design planning and development is an ongoing activity; all related activity is captured and documented on the corporate github repository. Planning, design input, design output, review and testing activities may all occur at any time. These activities are described below in Section 7, Design and Development Activities.

1. Design and Development **Planning Sessions**. Design and development planning happens during planning meetings, which may occur at any time. All decisions about what work is to be done in the sprint are captured in GitHub a issues folder. The results of the planning sessions are documented on GitHub.

2. **Requirements**. Requirements for a given piece of functionality are documented in a GitHub issue. Each issue has a unique URL. The requirement is typically summarized in the title of the issue or within the issue's description. 

1. **User interface design**. User Interface designs are documented and stored in Google Drive. All designs are available for public inspection. Only MDN employees can make changes to User Interface design documents. All revisions to design documents are maintained indefinitely by Google Drive and available at all times.

2. **Software design**. Where appropriate, software designs, including revisions to the designs, are documented in GitHub in the relevant repository. Other architecture documents may be stored in GitHub or Google Drive and will be linked to Jira issues. Software design may also be documented in the source code itself. All software design documentation including all revisions is maintained indefinitely in GitHub and Google Drive.

Most GitHub repositories represent an area of software functionality that is exposed to end users. Some repositories provide common functionality or test frameworks that may not be exposed to end users. 

The README file in each repository provides an overview of that repositories' purpose or functionality. 

The Master branch for each repository represents the latest software source code updates to that functionality. GitHub Tags are used to uniquely identify specific checkpoints of functionality; not all tags are deployed to production. For most products, tags are given semantic version numbers following this pattern: 

MAJOR.MINOR.PATCH, where

 * MAJOR version indicates changes for major new functionality or incompatible API changes,

 * MINOR version indicates when new functionality is added in a backwards-compatible manner, and

 * PATCH version indicates when backwards-compatible bug fixes are made.

For some products (such as the MDN Uploader), tags may only use MAJOR.MINOR numbering. In these cases, patch releases will cause the MINOR number to increment.

Software is typically only deployed from a tag created on the Master branch of a repository. Only in the rare case of an urgent/important "hotfix" will be a deployment be made from a tag created on a branch other than Master. That fix will later be incorporated into Master.


**Software Development**

Software developers develop, modify and test software on their local development workstation. 

Software changes can only be committed to the GitHub Master branch by a MDN employee or contractor (not by an open source developer). 

For all non-trivial changes, the software developer must seek review from another developer (known as reviewing a &quot;Pull Request&quot;) prior to committing to Master.

1. **Design History File (DHF)** The combination of Jira,, Google Docs, Zendesk, and GitHub together comprises the Design History File. See section 14 for details of the DHF.

2. **Development Responsibility** The CEO is responsible for the appropriateness, quality, processes and implementation of all development activities.

3. **Interfaces with Design Input.** All employees, contractors and consultants at MDN may interact with Design Input sources. Those sources are detailed in Section 8, Design Input.

**Updates**.

1. **Regular updates**. MDN software may be deployed at any time. Verification activities are conducted for each Jira issue (see sections 11 and 12 below). Validation activities are conducted for each new product released.

2. **Approval and Deployment (Design Transfer to Production)**. Deployment to production of customer-facing functionality must be approved by a VP-level employee or the CEO.


## Design Input

Consistent with 21 CFR 820.30 (c), each manufacturer shall establish and maintain procedures to ensure that the design requirements relating to a device are appropriate and address the intended use of the device, including the needs of the user and patient. The procedures shall include a mechanism for addressing incomplete, ambiguous, or conflicting requirements. The design input requirements shall be documented and shall be reviewed and approved by a designated individual(s). The approval, including the date and signature of the individual(s) approving the requirements, shall be documented.

It is MDN's policy and practice to capture designs in the form of two key artifacts:
1) Sequence Diagrams and 2) Swagger API Documents.

MDN has in its repository a collection of UML-style Sequence Diagrams showing the principal flows among all of the relevant components for each subflow.  These diagrams, when annoted with API and other reference information establishes both the current and planned design of the entire T1Pal system.

Standard RESTful APIs are the preferred means of inter-system communications.   These are best documented in the form of "Swagger" documents that completely define the API.

### Sources of Design Inputs.  

Input into the MDN design and development process, including requirements, may come from these sources, but is not limited to these sources:

* Interviews with actual and potential users MDN conducts in person, phone, video conference and email interviews with actual and potential users. The notes from these meetings are stored in Google Drive as Google Documents. Users include but are not limited to: people with diabetes, their care team, parents, doctors, diabetes educators, device makers and diabetes researchers.

* MDN Employees and Contractors**: MDN&#39;s employees, contractors and consultants may also be the source of design input.

* Observed and measured use of MDN  software: When running, MDN collects metrics and usage statistics. These data may also be sources of design input.

* Feedback from Alpha and Beta Users:  MDN collects feedback from Beta users as part of Software Validation activities (see section 11). Results from these activities may also be used as design input.

* Feedback received via social media, 
such as Twitter, Facebook, Instagram and comments on blog posts.

* Feedback from users via customer support, including emails to [support@t1pal.com](mailto:support@t1pal.com) and via our support ticketing system.

* Appropriateness of requirements to meet intended use:  It is the responsibility of the VP of Product or CEO to approve the appropriateness of product functionality that is made available via production servers. MDN developers may deploy code to non-production servers (such as &quot;staging&quot;, &quot;development&quot; or &quot;integration&quot; servers) without VP or CEO approval.

* Mechanism for addressing incomplete, ambiguous, or conflicting requirements:  Incomplete, ambiguous or conflicting requirements will be discussed during planning meetings and via ongoing conversation. It is the responsibility of the VP of Product or CEO to resolve incomplete, ambiguous or conflicting requirements for product functionality that is made available via production servers. The outcome of resolving these requirements issues is documented in Jira issues.

*  Review and approval:  Documentation for review and approval of all functionality is captured on Jira issues.

## Design Output

* Reference 21 CFR 820.30 (d):  Each manufacturer shall establish and maintain procedures for defining and documenting design output in terms that allow an adequate evaluation of conformance to design input requirements. Design output procedures shall contain or make reference to acceptance criteria and shall ensure that those design outputs that are essential for the proper functioning of the device are identified. Design output shall be documented, reviewed, and approved before release. The approval, including the date and signature of the individual(s) approving the output, shall be documented.

UML-styled Sequence Diagrams described above are used to capture design Outputs unambiguously and subject ot change control documentation.

* Evaluation of conformance to requirements.

* Verification and deployment of software:  Prior to deployment to production servers, software is deployed to a staging server environment where it is tested. The QA department is responsible for developing and executing verification tests (see section 10) although others including volunteer testers, other employees, and the CEO may also execute tests.

*  Documentation:

* All verification tests, both templates and executed tests, are documented in Google Docs and stored indefinitely in Google Drive, including a record of all changes to each file.

* Deployment of software to development, staging and production server environments is documented as a Jira list for each deployment.

* Review and approval**. The QA department is responsible for review and approval of all verification tests. VP-level or CEO approval is required for deployment to production servers.

## Design Review

* User interface reviews:  User interface designs are reviewed via Google Drive. Comments on designs in Google Drive are maintained in perpetuity.

* Code reviews:  All substantial changes to software source code intended to be deployed to production must be reviewed by a MDN employee other than the author of the source code. Review of design results.

* Review by individuals without direct responsibility:

* UI Design Review. All UI designs are reviewed by someone other than the UI designer.

* Code Review. An MDNs employee or contractor is responsible for reviewing all substantial code changes that will result in customer-facing functionality. The employee who proposed the changes (via GitHub pull request) may not review the proposed changes.

## Documentation

All relevant reviews are documented in Jira or Google Docs and stored in perpetuity in Google Drive. All changes and records, including the date and individuals performing the review, are maintained in perpetuity.

## Design Verification

* Black Box Test Templates: Black Box&quot; testing refers to test verification activities that are performed manually, not by automated code.
* Location, name and version:  Test verification templates are stored in Google Drive in folders with a unique name indicating the area being tested and the version number of the test. 
* Responsibility for tests:  Any MDN employee, contractor or consultant can create new &quot;Black 
Box&quot; tests.
* Changes to tests:  A record of changes to tests are maintained in perpetuity in the document version history for each test. Obsolete tests are prominently marked [OBSOLETE] and are moved to an archive directory.

* Executed tests:   For executed tests, the test template is copied to the &quot;Executed Verification Scripts&quot; folder where it is edited as the test is executed. Elements of the test are marked &quot;PASSED&quot; or &quot;FAILED.&quot; For elements of the test that have failed, a Jira issue is generated to address the issue.

* Automated &quot;White Box&quot; tests: At the discretion of the software developer, software functionality may be tested using automated tests.

* Software source code for the automated test suite will be stored in the same GitHub repository as the software functionality itself.

* If functionality includes an automated test or suite of tests, all tests must pass for the software source code can be merged into the &quot;master&quot; branch.

## Documentation

* Methods:   The method of verification is documented in the test verification template per Section 10.1. Links to each documented test are included in the DHF as described in Section 14.

* Date and Responsibility:  The date of running the verification test as well as the individuals performing the test are detailed in the executed test document per Section 10.2.

* Design Validation

* Defined operating conditions:  MDN software is intended to be used on computers and mobile devices with an Internet connection.

* Defined user needs and intended use: User needs are documented in requirements as per Section . The intended uses of MDN software are defined.

* Software validation:  The use of MDN software is validated by volunteer 

* Beta users. Beta users are selected to based on expressed interest in testing MDN software, configurations they have available (e.g. Mac or Windows, which diabetes devices they use), and demonstrated ability to complete homework assignments. Beta users are given homework assignments with instructions on how to test software functionality. Homework assignment templates are stored in the &quot;Validation Templates&quot; folder. Beta users document both quantitative and qualitative results of their use of the software in Google Docs. Those Google Docs are stored in Google Drive in the &quot;Validation Documentation&quot; folder. MDN  software is tested by Beta users with their own computers and mobile devices in their own actual use conditions.

## Risk analysis

A Risk Analysis review, consistent with chapter 4 "Risk and Hazard Management" is required before commencing Design Transfer.

## Design Transfer

* Consistent with 21 CFR 820.30 (h) each manufacturer shall establish and maintain procedures to ensure that the device design is correctly translated into production specifications.

* Transfer of development code to production. A software developer is assigned during the Sprint Planning meeting and identified on the github issue for implementation of the task. It is the responsibility of the software developer to implement the software per requirements detailed on the Jira issue or via UI design in Google Drive. If there are ambiguous requirements or designs, the ambiguity may be resolved through conversation. For substantial ambiguity, resolution will be documented in the Jira card. For minor changes or ambiguity, the resolution may be documented in the software code itself.

* Responsibility and Approval**. It is the responsibility of the VP of Product and/or CEO to assure that all requirements have been met, that designs have been correctly translated into Production, and that all appropriate verification and validation activities have been performed. VP of Product or CEO approval is required for deployment to Production of all substantial, customer-facing functionality.

**Documentation**. All development transfer activities are documented in githugithubb. For deployments to Production servers, a new Jira list will be created that contains the name, date and version number of software being deployed.


##  Design Changes

* Reference 21 CFR 820.30 (i) Design changes: Each manufacturer shall establish and maintain procedures for the identification, documentation, validation or where appropriate verification, review, and approval of design changes before their implementation.

* Iteration of Design Changes:  MDN uses an agile development model. Design changes may occur in any sprint. In addition to documenting design as described above in Section 7, Design and Development Activities, ongoing changes to design will be documented as described below.

* Identification:  All documents in  GitHub are uniquely identified by a unique Uniform Resource Identifier (URI) that is assigned by the respective service. Documents may additionally have a human-readable document title and document ID. For example, this document is:

##   Documentation of design changes.

* All changes to requirements, design, software source code, functionality, verification and validation are documented and tracked in Jira, Pixelapse, GitHub and Google Docs. Revision history is maintained in perpetuity.

* Changes to requirements are identified and documented in github issues. A history of changes to github issues is maintained in perpetuity.

* Changes to software source code are maintained in GitHub. Revision history is maintained in perpetuity.

* Review and Approval:  Design changes are reviewed and approved before deployment to production. All review and approval will be documented in Jira, Pixelapse, GitHub or Google Docs.

##  Design History File (DHF)

*  Reference 21 CFR 820.30 (j) Design history file: Each manufacturer shall establish and maintain a DHF for each type of device. The DHF shall contain or reference the records necessary to demonstrate that the design was developed in accordance with the approved design plan and the requirements of this part.
*  Together, the documentation maintained in GitHub comprises each MDN product&#39;s Design History File (DHF).

##  CFR Reference: 21 CFR 820.30 Design Controls

* Design and development planning: Each manufacturer shall establish and maintain plans that describe or reference the design and development activities and define responsibility for implementation. The plans shall identify and describe the interfaces with different groups or activities that provide, or result in, input to the design and development process. The plans shall be reviewed, updated, and approved as design and development evolves.

* Design input:  Each manufacturer shall establish and maintain procedures to ensure that the design requirements relating to a device are appropriate and address the intended use of the device, including the needs of the user and patient. The procedures shall include a mechanism for addressing incomplete, ambiguous, or conflicting requirements. The design input requirements shall be documented and shall be reviewed and approved by a designated individual(s). The approval, including the date and signature of the individual(s) approving the requirements, shall be documented.

* Design output: Each manufacturer shall establish and maintain procedures for defining and documenting design output in terms that allow an adequate evaluation of conformance to design input requirements. Design output procedures shall contain or make reference to acceptance criteria and shall ensure that those design outputs that are essential for the proper functioning of the device are identified. Design output shall be documented, reviewed, and approved before release. The approval, including the date and signature of the individual(s) approving the output, shall be documented.

* Design review: Each manufacturer shall establish and maintain procedures to ensure that formal documented reviews of the design results are planned and conducted at appropriate stages of the device&#39;s design development. The procedures shall ensure that participants at each design review include representatives of all functions concerned with the design stage being reviewed and an individual(s) who does not have direct responsibility for the design stage being reviewed, as well as any specialists needed. The results of a design review, including identification of the design, the date, and the individual(s) performing the review, shall be documented in the design history file (the DHF).

* Design verification:  Each manufacturer shall establish and maintain procedures for verifying the device design. Design verification shall confirm that the design output meets the design input requirements. The results of the design verification, including identification of the design, method(s), the date, and the individual(s) performing the verification, shall be documented in the DHF.

* Design validation:  Each manufacturer shall establish and maintain procedures for validating the device design. Design validation shall be performed under defined operating conditions on initial production units, lots, or batches, or their equivalents. Design validation shall ensure that devices conform to defined user needs and intended uses and shall include testing of production units under actual or simulated use conditions. Design validation shall include software validation and risk analysis, where appropriate. The results of the design validation, including identification of the design, method(s), the date, and the individual(s) performing the validation, shall be documented in the DHF.

* Design transfer:  Each manufacturer shall establish and maintain procedures to ensure that the device design is correctly translated into production specifications.

* Design changes:  Each manufacturer shall establish and maintain procedures for the identification, documentation, validation or where appropriate verification, review, and approval of design changes before their implementation.

* Design history file:  Each manufacturer shall establish and maintain a DHF for each type of device. The DHF shall contain or reference the records necessary to demonstrate that the design was developed in accordance with the approved design plan and the requirements of this part.


## T1Pal Definitive List of Intended Use Cases

This document provides the list of Intended Use cases for T1Pal.

These Intended Use cases together with additional requirements listed below,
convey the T1Pal system requirements that will be the target of validation for each and every release. 

Altogether, the three Intended Use cases, and the Additional System Requirements below, together with the present Quality Management system, T1Pal should meet FDA all of the rules for clearance -- using the de novo pathway, and the T1Pal realization of "Special Controls" enumerated in 2005.


### REQ_1010 -- Secondary Display
It is an intended use for T1Pal to receive data from one or more medical devices and provide a secondary 
display of the data.

### REQ_1020 -- Remote Access

It is an intended use that authorized "followers" will have access to a secondary display of the same data.

### REQ_1030 -- Technical Support

It is intended that the display of secondary data will be used to provide "Technical Support."  "Technical Support" in this
case is limited to providing documentation that may support 
* device warranty claims, 
* guidance on replacement of devices or consumables, and 
*acts
to remedy impairments to requisite data communications.

## Additional System Requirements

In addition to delivering the capabilities for intended use above, the following additional system requirements are targets of validation for each release.

### REQ_2010 -- Data Privacy and Modification Protections

The T1Pal is intended to be HIPPA compliant with respect to privacy and access to data.

### REQ_2020 -- Protection against modification of data.

The T1Pal is intended to protect against modification of data provided for secondary display.

### REQ_2030 -- T1Pal Labelling

The T1Pal software shall provide clear and unambiguous labelling that describes both intended use, and warnings against all other uses.




##  References

1.  U.S. Food and Drug Administration, 21 CFR Part 820: Quality System Regulation.
2.  General Principles of Software Validation; Final Guidance for Industry and FDA Staff
3.  AAMI TIR45:2012 Technical Information Report Guidance on the use of AGILE practices in the development of medical device softwareOverview


## **Operations Management**

The T1Pal solution is in fact an interworking set of services that are each somewhat independent of each other.   The run-book described above is used to direct operations staff to reports,  displays of data flows, lists of resources consumed, and response times for specified components.

The operations staff must monitor all displays and reports continuously 24 x 7 x 365 and at the same time monitor trouble ticket complaints.

In the event of an outage of any kind, the outage must be documented on freshstatus.com web site so as to alert customers subscribing to that service.
https://t1pal-995.freshstatus.io/   Any and all observed impairments to any T1Pal components should be entered into a trouble ticket.  The trouble ticket system is configured to receive emails directed to support@t1pal.com   The trouble ticketing system is at  t1pal.helpy.io


### *HIPAA Compliance*

We ensure compliance with HIPAA, MDN protects the information from patients in several ways. In particular, we strive to:

* Ensure confidentially 
* Protect against security threats and unauthorized disclosure. 
* Validate the integrity of information 
* Establish secure processes and ensure that our workforce is in compliance.

* Communicate -- All information that is transferred to and from the MDN platform is encrypted in transit. In particular, MDN servers communicating using "TLS" and reject any attempts to communicate using unencrypted connections. 

* Storage -- All data stored on permanent storage systems is encrypted with industry standard encryption.

* Physical Security 
  MDN servers are part of Amazon's AWS compute cloud, which is compliant with the US Government's FedRamp standards for physical and electronic data security. AWS enables covered entities and their business associates subject to HIPAA to leverage the secure AWS environment to process, maintain, and store protected health information. 

The Amazon whitepaper on HIPAA provides a list of best practices, which MDN is following. 

* Deployment Security -- Encryption and deploy keys are stored separately from customer data access is tightly controlled. 
* Integrity -- All user data is traceable and auditable. Every transaction in the database is recorded with a cryptographically secure identifier in the database (a "hash").


We also follow all HIPAA guidelines for organizational policy: 

* Ben West (bewest@medicaldatanetworks.com) is our privacy officer and is accountable for HIPAA compliance. 
* Patients have the right to acces all of their PHI, in real time, in both human-readable and machine-accessible forms. This is much faster than the HIPAA-required 30 days). 
* All employees are trained on their responsibilities with respect to HIPAA. 
* All access to PHI is limited and logged. Users can request that their data be deleted at any time.

MDN privacy policy and terms are published on the T1Pal web site under /policy and /terms.

In the event of a breach, we will notify affected users via the MDN Breach Notification Letter

