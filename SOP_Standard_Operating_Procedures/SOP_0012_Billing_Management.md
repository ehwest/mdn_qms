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
# Billing Management

MDN shall conduct its product selection process, invoicing, and other billing operations so
as to maintain privacy requirements of both HIPAA and PCI (payment card industry) demands.
The following sections identify how this is accomplished.

## Credit Card Service Operations
"Stripe.com" and "Servicebot.io" are providers of billing services to T1Pal operations.
These providers are separate and independent companies that provide all of the credit card and related payment
services to T1Pal software operations.
All communications between T1Pal, and subscribers, to/from these providers is encrypted using standard SSL methods.

There are functions of stripe.com that fail to completely meet PCI demands for credit card handling. 
This issue is well known and was created when stripe.com introduced advanced analysis of
stripe.com customer behaviors in an "SQL" engine.
The remedy for these has been accepted and planned by stripe.com.

Generally, processing payments 
through a credit card processor creates personally identifiable information (PII) that must be secured both in transmission and storage.
However, US Health and Human Services (HHS) have stated that collecting payments is excluded explicitly from HIPAA mandates.

For T1Pal to continue to utilize Stripe for invoicing, and financial analysis, T1Pal will need to get a Business Associate Agreement (BAA)
from Stripe, and configure use of Stripe to comply with HIPAA requirements.
A BAA template is expected in follow-on revisions to this QMS.

In addition, Payment Card Industry Data Security Standards (PCI DSS).
sets the minimum standard for credit card data security, and requires a periodic audit of security operations.
T1Pal expects to achieve PCI Level 4 compliance, which includes use of a checklist and an annual audit.  Both the checklist
and actual audit results will be managed in revisions to this QMS.
