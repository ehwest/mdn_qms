---
repository: "github.com/ehwest/mdn_qms"
folder: "mdn_qms/SOP_Standard_Operating_Procedures"
title: "SOP_0007 Access Controls for Software -- GitHub Utilization"
document_id: "SOP-0007"
authors:
- github.com/ehwest
approvers:
- github.com/bewest
revision: "05"
approval_date: "2020-07-18"
effective_date: "2020-07-18"
content_type: concept
description: "SOP 0007 Access controls for Software -- Github Utilization"
---
## 1. Purpose

This document and supporting references establish a standard operating procedure for the design and development of new, or redesign of existing, Medical Data Networks software and its release to market.

## 2. Scope

This applies to all medical and research software devices designed and developed by Medical Data Networks LLC.

## 4. Tools

The following tools are currently in use by Medical Data Networks:

1.  **GitHub**. [GitHub](https://www.github.com/) is the sole tool for storage of all permanent documents, drawings, agreements, and software.   

All software for all components, regardless of their provenance or use, is stored and versioned in one or more named GitHub "repositories" owned by Medical Data Networks, LLC. and is under access control by its officers and designated employees.   

This specifically includes all documents related to Medical Data Networks' quality management system, and includes all open-sourced and/or commercial software components.  GitHub also maintains a complete set of components applicable to the several different versions of software:  Production, Staging, and Development.   

Because GitHub is a distributed storage system, the computers used by all of the company officers, and software developers, and engineers is configured to store and access the complete set of GitHub repositories used by the firm.   Therefore, no specific backup resource or procedure --outside of GitHub-- is needed or used.

This approach enables each and every authorized employee and/or contractor to review the current, planned, and past revision history on all documents, software, and records.


2.  **Google Email, Docs and Google Drive**. 

[https://docs.google.com](http://docs.google.com/) 
and
[https://drive.google.com](http://drive.google.com/) 
and 
[https://gmail.com](http://gmail.com/) 

are each used only informally as an aid to intra company communications.  

No quality management system documents, or artifacts associated with any business process are permanently stored on Google Docs.  All authoritative and/or permant documents are retained in the appropriate GitHub repository.

3. **Amazon Web Services (AWS)**. [https://aws.amazon.com](https://aws.amazon.com/). AWS is one of the cloud providers used by Medical Data Networks.  Selected production Medical Data Networks software is deployed to AWS. Medical Data Networks also maintains non-production servers used to test software under development (&quot;dev&quot; environment) and ready to be deployed after acceptance testing (&quot;staging environment).

4. **Digital Ocean**. [Digital Ocean](https://digitalocean.com)  is one of the cloud providers used by Medical Data Networks.  Selected production Medical Data Networks software is deployed to Digital Ocean. Medical Data Networks also maintains non-production servers used to test software under development (&quot;dev&quot; environment) and ready to be deployed after acceptance testing and staging environment).

5. **Software Reliability Estimator (SRE)**. [SRE](https://github.com/ehwest/sre)  is a containerized software tool that is used to estimate the Software Reliability of all major releases of services and/or software code, prior to public release.  this tool computes the parameters of a statistical model of all issues that have emerged in the preparation of a software release, enabling a reliable reliability estimate to be computed.   In the event the SRE results fall below pre-defined standards, additional testing will be required prior to software release to the public.

**Backups and disaster recovery**.

1. All Google Drive contents are  backed up in Google Vault.
2. All Google Drive and Google Vault backups are retained in perpetuity.
3. All email is stored via Google Apps email and automatically backed up in Google Vault and is retained in perpetuity (including deleted emails).
4. Redundant and duplicative distribution of GitHub-based repositories are retained on the primary computers of all officers, developers, and engineers.  This eliminates the need for a separate and independent back up system.  All of the software, documents, etc. are stored in the distributed GitHub-based system.


## Design and Development Planning

1. Reference 21 CFR 820.30 (b): Design and development planning. 

Each manufacturer shall establish and maintain plans that describe or reference the design and development activities and define responsibility for implementation. The plans shall identify and describe the interfaces with different groups or activities that provide, or result in, input to the design and development process. The plans shall be reviewed, updated, and approved as design and development evolves.

2. **Design and Development Planning Activities.** Medical Data Networks uses an iterative, agile development process. Design planning and development is an ongoing activity; all related activity is captured and documented on Jira issues.. Planning, design input, design output, review and testing activities may all occur at any time. These activities are described below in Section 7, Design and Development Activities.

## Design and Development Activities

1. Design and Development **Planning Sessions**. Design and development planning happens during planning meetings, which may occur at any time. All decisions about what work is to be done in the sprint are captured in GitHub a issues folder. The results of the planning sessions are documented on GitHub.

2. **Requirements**. Requirements for a given piece of functionality are documented in a GitHub issue. Each issue has a unique URL. The requirement is typically summarized in the title of the issue or within the issue's description. 

**Design Activities**

1. **User interface design**. User Interface designs are documented and stored in Google Drive. All designs are available for public inspection. Only Medical Data Networks employees can make changes to User Interface design documents. All revisions to design documents are maintained indefinitely by Google Drive and available at all times.

2. **Software design**. Where appropriate, software designs, including revisions to the designs, are documented in GitHub in the relevant repository. Other architecture documents may be stored in GitHub or Google Drive and will be linked to Jira issues. Software design may also be documented in the source code itself. All software design documentation including all revisions is maintained indefinitely in GitHub and Google Drive.

**Development Activities.**

1. **Development Tools**. See section 5.

2. **GitHub repositories.** 

Most GitHub repositories represent an area of software functionality that is exposed to end users. Some repositories provide common functionality or test frameworks that may not be exposed to end users. 

The README file in each repository provides an overview of that repositories' purpose or functionality. 

The Master branch for each repository represents the latest software source code updates to that functionality. GitHub Tags are used to uniquely identify specific checkpoints of functionality; not all tags are deployed to production. For most products, tags are given semantic version numbers following this pattern: MAJOR.MINOR.PATCH, where

 * MAJOR version indicates changes for major new functionality or incompatible API changes,

 * MINOR version indicates when new functionality is added in a backwards-compatible manner, and

 * PATCH version indicates when backwards-compatible bug fixes are made.

For some products (such as the Medical Data Networks Uploader), tags may only use MAJOR.MINOR numbering. In these cases, patch releases will cause the MINOR number to increment.

Software is typically only deployed from a tag created on the Master branch of a repository. Only in the rare case of an urgent/important &quot;hotfix&quot; will be a deployment be made from a tag created on a branch other than Master. That fix will later be incorporated into Master.

**Software Development**

Software developers develop, modify and test software on their local development workstation. 

Software changes can only be committed to the GitHub Master branch by a Medical Data Networks employee or contractor (not by an open source developer). 

For all non-trivial changes, the software developer must seek review from another developer (known as reviewing a &quot;Pull Request&quot;) prior to committing to Master.

1. **Design History File (DHF)** The combination of Jira,, Google Docs, Zendesk, and GitHub together comprises the Design History File. See section 14 for details of the DHF.

2. **Development Responsibility** The CEO is responsible for the appropriateness, quality, processes and implementation of all development activities.

3. **Interfaces with Design Input.** All employees, contractors and consultants at Medical Data Networks may interact with Design Input sources. Those sources are detailed in Section 8, Design Input.

**Updates**.

1. **Regular updates**. Medical Data Networks software may be deployed at any time. Verification activities are conducted for each Jira issue (see sections 11 and 12 below). Validation activities are conducted for each new product released.

2. **Approval and Deployment (Design Transfer to Production)**. Deployment to production of customer-facing functionality must be approved by a VP-level employee or the CEO.

## Design Input

1. **Reference 21 CFR 820.30 (c):** Each manufacturer shall establish and maintain procedures to ensure that the design requirements relating to a device are appropriate and address the intended use of the device, including the needs of the user and patient. The procedures shall include a mechanism for addressing incomplete, ambiguous, or conflicting requirements. The design input requirements shall be documented and shall be reviewed and approved by a designated individual(s). The approval, including the date and signature of the individual(s) approving the requirements, shall be documented.

2. **Sources of Design Inputs.** Input into the design and development process, including requirements, may come from these sources, but is not limited to these sources:

3. **Interviews with actual and potential users**. Medical Data Networks conducts in person, phone, video conference and email interviews with actual and potential users. The notes from these meetings are stored in Google Drive as Google Documents. Users include but are not limited to: people with diabetes, their care team, parents, doctors, diabetes educators, device makers and diabetes researchers.

4. **Medical Data Networks Employees and Contractors**. Medical Data Networks&#39;s employees, contractors and consultants may also be the source of design input.

5. **Observed and measured use of Medical Data Networks software**. When running, Medical Data Networks collects metrics and usage statistics. These data may also be sources of design input.

6. **Feedback from Alpha and Beta Users**. Medical Data Networks collects feedback from Beta users as part of Software Validation activities (see section 11). Results from these activities may also be used as design input.
 * Feedback received via social media, such as Twitter, Facebook, Instagram and comments on blog posts.
 * Feedback from users via customer support, including emails to [support@tidepool.org](mailto:support@tidepool.org) and via our support ticketing system.

7. **Appropriateness of requirements to meet intended use**. It is the responsibility of the VP of Product or CEO to approve the appropriateness of product functionality that is made available via production servers. Medical Data Networks developers may deploy code to non-production servers (such as &quot;staging&quot;, &quot;development&quot; or &quot;integration&quot; servers) without VP or CEO approval.

8. **Mechanism for addressing incomplete, ambiguous, or conflicting requirements**. Incomplete, ambiguous or conflicting requirements will be discussed during planning meetings and via ongoing conversation. It is the responsibility of the VP of Product or CEO to resolve incomplete, ambiguous or conflicting requirements for product functionality that is made available via production servers. The outcome of resolving these requirements issues is documented in Jira issues.

9. **Review and approval**. Documentation for review and approval of all functionality is captured on Jira issues.

## Design Output

1. **Reference 21 CFR 820.30 (d):** Each manufacturer shall establish and maintain procedures for defining and documenting design output in terms that allow an adequate evaluation of conformance to design input requirements. Design output procedures shall contain or make reference to acceptance criteria and shall ensure that those design outputs that are essential for the proper functioning of the device are identified. Design output shall be documented, reviewed, and approved before release. The approval, including the date and signature of the individual(s) approving the output, shall be documented.

2. **Evaluation of conformance to requirements**.

3. **Verification and deployment of software**. 

Prior to deployment to production servers, software is deployed to a staging server environment where it is tested. The QA department is responsible for developing and executing verification tests (see section 10) although others including volunteer testers, other employees, and the CEO may also execute tests.

**Documentation**.

1. All verification tests, both templates and executed tests, are documented in Google Docs and stored indefinitely in Google Drive, including a record of all changes to each file.

2. Deployment of software to development, staging and production server environments is documented as a Jira list for each deployment.

3. **Review and approval**. The QA department is responsible for review and approval of all verification tests. VP-level or CEO approval is required for deployment to production servers.

## Design Review

1, **Review**.
 * **User interface reviews**. User interface designs are reviewed via Google Drive. Comments on designs in Google Drive are maintained in perpetuity.
 * **Code reviews**. All substantial changes to software source code intended to be deployed to production must be reviewed by a Medical Data Networks employee other than the author of the source code. Review of design results.
 * **Review by individuals without direct responsibility.**
  - UI Design Review. All UI designs are reviewed by someone other than the UI designer.
  - Code Review. A Medical Data Networks employee or contractor is responsible for reviewing all substantial code changes that will result in customer-facing functionality. The employee who proposed the changes (via GitHub pull request) may not review the proposed changes.

 * **Documentation.** 

All relevant reviews are documented in Jira or Google Docs and stored in perpetuity in Google Drive. All changes and records, including the date and individuals performing the review, are maintained in perpetuity.

## Design Verification

 * **Black Box&quot; Test Templates**.
 * **Black Box&quot; testing** refers to test verification activities that are performed manually, not by automated code.
 * **Location, name and version**. Test verification templates are stored in Google Drive in folders with a unique name indicating the area being tested and the version number of the test. For example:
 Test Script Template | Blip - Data Visualization Module: Device Settings | 1.0

 * **Responsibility for tests**. Any Medical Data Networks employee, contractor or consultant can create new &quot;Black 
Box&quot; tests.
  - **Changes to tests**. A record of changes to tests are maintained in perpetuity in the document version history for each test. Obsolete tests are prominently marked [OBSOLETE] and are moved to an archive directory.

  - **Executed tests**. For executed tests, the test template is copied to the &quot;Executed Verification Scripts&quot; folder where it is edited as the test is executed. Elements of the test are marked &quot;PASSED&quot; or &quot;FAILED.&quot; For elements of the test that have failed, a Jira issue is generated to address the issue.

  - **Automated &quot;White Box&quot; tests.**

   * At the discretion of the software developer, software functionality may be tested using automated tests.

   * Software source code for the automated test suite will be stored in the same GitHub repository as the software functionality itself.
   * If functionality includes an automated test or suite of tests, all tests must pass for the software source code can be merged into the &quot;master&quot; branch.

_1. **Documentation**.
__1. **Methods**. The method of verification is documented in the test verification template per Section 10.1. Links to each documented test are included in the DHF as described in Section 14.
__2. **Date and Responsibility**. The date of running the verification test as well as the individuals performing the test are detailed in the executed test document per Section 10.2.

## Design Validation

1. **Defined operating conditions**. Medical Data Networks software is intended to be used on computers and mobile devices with an Internet connection.

2. **Defined user needs and intended uses**. User needs are documented in requirements as per Section . The intended uses of Medical Data Networks software are defined in [DOC-0001 Intended Uses](https://docs.google.com/document/d/1e4Q3yCbTC6J39RO1VKvVBn0BAgT4FXmC-2seiLz_6wQ/edit#heading=h.ua8jssuxs2x).
3. **Software validation**. The use of Medical Data Networks is software is validated by volunteer Beta users. Beta users are selected to based on expressed interest in testing Medical Data Networks software, configurations they have available (e.g. Mac or Windows, which diabetes devices they use), and demonstrated ability to complete homework assignments. Beta users are given homework assignments with instructions on how to test software functionality. Homework assignment templates are stored in the &quot;Validation Templates&quot; folder. Beta users document both quantitative and qualitative results of their use of the software in Google Docs. Those Google Docs are stored in Google Drive in the &quot;Validation Documentation&quot; folder. Medical Data Networks software is tested by Beta users with their own computers and mobile devices in their own actual use conditions.
4. **Risk analysis**. Risks analysis and mitigation processes are documented in [DOC-0002 Risk Analysis and Mitigation](https://docs.google.com/document/d/17mb--4AeFVAgNJLEIE6obXIVjeu0ST7i2cYAsziu8Vc/edit).
5. **Documentation**. Any changes to design requirements or software is documented in design history file (DHF) per Section 13.


## Design Transfer

1. **Reference 21 CFR 820.30 (h) Design transfer**. Each manufacturer shall establish and maintain procedures to ensure that the device design is correctly translated into production specifications.

2. **Transfer of development code to production**. A software developer is assigned during the Sprint Planning meeting and identified on the Jira issue for implementation of the task. It is the responsibility of the software developer to implement the software per requirements detailed on the Jira issue or via UI design in Google Drive. If there are ambiguous requirements or designs, the ambiguity may be resolved through conversation. For substantial ambiguity, resolution will be documented in the Jira card. For minor changes or ambiguity, the resolution may be documented in the software code itself.

3 **Responsibility and Approval**. It is the responsibility of the VP of Product and/or CEO to assure that all requirements have been met, that designs have been correctly translated into Production, and that all appropriate verification and validation activities have been performed. VP of Product or CEO approval is required for deployment to Production of all substantial, customer-facing functionality.

4 **Documentation**. All development transfer activities are documented in Jira. For deployments to Production servers, a new Jira list will be created that contains the name, date and version number of software being deployed.


## Design Changes

1. **Reference 21 CFR 820.30 (i) Design changes**. Each manufacturer shall establish and maintain procedures for the identification, documentation, validation or where appropriate verification, review, and approval of design changes before their implementation.

2. **Iteration of Design Changes.** Medical Data Networks uses an agile development model. Design changes may occur in any sprint. In addition to documenting design as described above in Section 7, Design and Development Activities, ongoing changes to design will be documented as described below.

3. **Identification**. All documents in Jira, Pixelapse, GitHub and Google Docs are uniquely identified by a unique Uniform Resource Identifier (URI) that is assigned by the respective service. Documents may additionally have a human-readable document title and document ID. For example, this document is:

**URI** : https://docs.google.com/a/tidepool.org/document/d/
 19vWtyDNesVyxE5gKXwppgRGWvn-EXrttCLJH5nRys1U
**Human-readable Document ID** : SOP-0005
**Human-readable Title** : Design, Development and Release
 
 4. **Documentation of design changes**.
    1. All changes to requirements, design, software source code, functionality, verification and validation are documented and tracked in Jira, Pixelapse, GitHub and Google Docs. Revision history is maintained in perpetuity.
    2. Changes to requirements are identified and documented in Jira issues. A history of changes to Jira issues is maintained in perpetuity.
    3. Changes to UI designs are maintained in Pixelapse. Revision history is maintained in perpetuity.
    4. Changes to software source code are maintained in GitHub. Revision history is maintained in perpetuity.
    5. Changes to Google Docs. If design changes are documented in Google Docs, changes and revision history to those documents will be maintained in perpetuity and stored in the &quot;Medical Data Networks Quality System&quot; folder in Google Drive.
    6. **Review and Approval.** Design changes are reviewed and approved before deployment to production. All review and approval will be documented in Jira, Pixelapse, GitHub or Google Docs.

## Design History File (DHF)

  1. **Reference 21 CFR 820.30 (j) Design history file**. Each manufacturer shall establish and maintain a DHF for each type of device. The DHF shall contain or reference the records necessary to demonstrate that the design was developed in accordance with the approved design plan and the requirements of this part.
  2. Together, the documentation maintained in Jira, Zendesk, GitHub and Google Docs comprises each Tidepool product&#39;s Design History File (DHF).

## CFR Reference: 21 CFR 820.30 Design Controls

**(a) Design and development planning**. Each manufacturer shall establish and maintain plans that describe or reference the design and development activities and define responsibility for implementation. The plans shall identify and describe the interfaces with different groups or activities that provide, or result in, input to the design and development process. The plans shall be reviewed, updated, and approved as design and development evolves.

**(b) Design input**. Each manufacturer shall establish and maintain procedures to ensure that the design requirements relating to a device are appropriate and address the intended use of the device, including the needs of the user and patient. The procedures shall include a mechanism for addressing incomplete, ambiguous, or conflicting requirements. The design input requirements shall be documented and shall be reviewed and approved by a designated individual(s). The approval, including the date and signature of the individual(s) approving the requirements, shall be documented.

**(c) Design output**. Each manufacturer shall establish and maintain procedures for defining and documenting design output in terms that allow an adequate evaluation of conformance to design input requirements. Design output procedures shall contain or make reference to acceptance criteria and shall ensure that those design outputs that are essential for the proper functioning of the device are identified. Design output shall be documented, reviewed, and approved before release. The approval, including the date and signature of the individual(s) approving the output, shall be documented.

**(d) Design review**. Each manufacturer shall establish and maintain procedures to ensure that formal documented reviews of the design results are planned and conducted at appropriate stages of the device&#39;s design development. The procedures shall ensure that participants at each design review include representatives of all functions concerned with the design stage being reviewed and an individual(s) who does not have direct responsibility for the design stage being reviewed, as well as any specialists needed. The results of a design review, including identification of the design, the date, and the individual(s) performing the review, shall be documented in the design history file (the DHF).

**(e) Design verification**. Each manufacturer shall establish and maintain procedures for verifying the device design. Design verification shall confirm that the design output meets the design input requirements. The results of the design verification, including identification of the design, method(s), the date, and the individual(s) performing the verification, shall be documented in the DHF.

**(f) Design validation**. Each manufacturer shall establish and maintain procedures for validating the device design. Design validation shall be performed under defined operating conditions on initial production units, lots, or batches, or their equivalents. Design validation shall ensure that devices conform to defined user needs and intended uses and shall include testing of production units under actual or simulated use conditions. Design validation shall include software validation and risk analysis, where appropriate. The results of the design validation, including identification of the design, method(s), the date, and the individual(s) performing the validation, shall be documented in the DHF.

**(g) Design transfer**. Each manufacturer shall establish and maintain procedures to ensure that the device design is correctly translated into production specifications.

**(h) Design changes**. Each manufacturer shall establish and maintain procedures for the identification, documentation, validation or where appropriate verification, review, and approval of design changes before their implementation.

**(i) Design history file**. Each manufacturer shall establish and maintain a DHF for each type of device. The DHF shall contain or reference the records necessary to demonstrate that the design was developed in accordance with the approved design plan and the requirements of this part.


## 3.  References

1. U.S. Food and Drug Administration, 21 CFR Part 820: Quality System Regulation.
2. General Principles of Software Validation; Final Guidance for Industry and FDA Staff
3. AAMI TIR45:2012 Technical Information Report Guidance on the use of AGILE practices in the development of medical device softwareOverview
