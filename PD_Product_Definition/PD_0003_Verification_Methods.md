---
repository: "github.com/ehwest/mdn_qms"
folder: "PD"
title: "PD_0003_Verification_Methods.md"
document_id: "PD_0003"
authors:
- github.com/ehwest
approvers:
- github.com/bewest
revision: "05"
approval_date: "2020-08-24"
effective_date: "2020-08-24"
description: "T1Pal Verification Methods"
---

# Verification 

The FDA web site providing quality system regulations [Part 20, CFR 820]( https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfcfr/CFRSearch.cfm?CFRPart=820)
defines product verification as ensuring
*each element* of a device meets the appropriate specifications and standards.
The focus on Verification is therefore on each element of a device, and
the demonstration that each such element meets design specifications and standards.

Software verification provides objective evidence that the design outputs of a particular phase of the software development life cycle meet all of the specified requirements for that phase. 

Software verification looks for consistency, completeness, and correctness of the software and its supporting documentation, as it is being developed, and provides support for a subsequent conclusion that software is validated. 

Software testing is one of many verification activities intended to confirm that software development output meets its input requirements. Other verification activities include various static and dynamic analyses, code and document inspections, walkthroughs, and other techniques.

Because the T1Pal software is a collection of "micro-services" the approach for
product verification is largely accomplished by a technical review of
each of the component micro-services as implemented in code.

Each such micro-service is (and shall be) be developed together with a suite of tests for testing
each and every micro-service.  The tests for each such micro-service are intended to be
comprehensive, including all known logical states traversed in use of the overall T1pal product.


## Responsibilities

1. The CEO and VP-level employees are responsible for overseeing and maintaining this standard operating procedure and for assuring that all employees are trained in its requirements.
2. It is the responsibility of all employees, contractors and departments at Medical Data Networks to adhere to this procedure.
