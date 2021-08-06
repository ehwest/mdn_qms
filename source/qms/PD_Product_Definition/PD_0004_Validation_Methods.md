---
repository: "github.com/ehwest/mdn_qms"
folder: "PD_Product_Definition"
title: "PD_0004_Validation_Methods"
authors:
- github.com/ehwest
approvers:
- github.com/bewest
approval_date: "2020-10-01"
---


# Software Validation Defined

The FDA [PD_Product_Definition/General-Principles-of-Software-Validation---Final-Guidance-for-Industry-and-FDA-Staff.pdf](https://github.com/ehwest/mdn_qms/blob/master/PD_Product_Definition/General-Principles-of-Software-Validation---Final-Guidance-for-Industry-and-FDA-Staff.pdf)

Software validation is a part of the design validation for a finished device, but is not separately defined in the Quality System regulation. 

For purposes of this guidance, FDA considers software validation to be “confirmation by examination and provision of objective evidence that software specifications conform to user needs and intended uses, and that the particular requirements implemented through software can be consistently fulfilled.” 

In practice, software validation activities may occur both during, as well as at the end of the software development life cycle to ensure that all requirements have been fulfilled. Since software is usually part of a larger hardware system, the validation of software typically includes evidence that all software requirements have been implemented correctly and completely and are traceable to system requirements. 

A conclusion that software is validated is highly dependent upon comprehensive software testing, inspections, analyses, and other verification tasks performed at each stage of the software development life cycle. Testing of device software functionality in a simulated use environment, and user site testing are typically included as components of an overall design validation program for a software automated device.


The following table of T1Pal use-cases shows the principle method to be used to validate the T1Pal product.


|Use Case|Approach|Method|
|-----------------------------|---------------------------|------------------------|
|REQ_1000 Secondary Display|Inspection   |Code Review by Engineering Team|
|REQ_1010 Remote Access    |Demonstration|Execute End-to-End Dynamic Test Suite|
|REQ_1020 Documentation Support|Demonstration|Execute End-to-End Dynamic Test Suite|
|REQ_1030 Technical Support|Demonstration|Execute End-to-End Dynamic Test Suite|


# Code Review by Engineering Team

This method of verification is accomplished by management hosting a code-review
of all of the components of the software used to enable secondary display of data.
The code review requires a joint enumeration of the principle software and/or service
components in the technical solution for secondary display.
Then, for each software/service component, the team is expecte to carefully review
the code and document its approval.

It is important to note that an output of this code review by the engineering time,
will produce a definitive list of micro-services that are part of the T1Pal product.
In addition, evidence of code verification tests (that may be automated tests) have
executed successfully is part of this review.


# Execute End-to-End Dynamic Test Suite

This method of verification is accomplished by using test data sets to
create outputs that can be inspected for accuracy and completeness.
Test data sets are created as part of the code review by the engineering team,
and focus on criteria that define "passing" for each of the tested
use-cases.

Test data sets shall include at least one data set derived from actual patient
secondary display data.  In addition, a second data set derived from extreme conditions
not like that of an actual patient shall be used to test for out-of-limits results.



Part 20, CFR 820 defines product validation as ensuring 
the T1Pal product
delivers on the intended use.
Product element verification is described in PD_0004_Product_Component_Verification.




