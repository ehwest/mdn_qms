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
# Performance Management

For all software services provided via API, "health check" probes shall be provided to measure the response time of the API under load.  The response time should include measures of internal "real-world" function of the API, preferably using test credentials that fully test database connectivity, database functions, and health checks of subtending API services.

Time series logs of health check calls shall be logged for the most recent 30 days.  Tools to use the logs to display charts and graphs shall be provided with the deployment of new API versions.



## References

1. [21 CFR 820](https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfcfr/CFRSearch.cfm?CFRPart=820&amp;showFR=1&amp;subpartNode=21:8.0.1.1.12.13)
2. [FDA](https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfcfr/CFRSearch.cfm?CFRPart=820&amp;showFR=1&amp;subpartNode=21:8.0.1.1.12.13)
3.  [Quality System Regulation](https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfcfr/CFRSearch.cfm?CFRPart=820&amp;showFR=1&amp;subpartNode=21:8.0.1.1.12.13)
4. ISO 13485:2016 Clause 4.2.5

## Requirements
MDN shall provide a dashboard showing the current performance status of the T1Pal operation.  The intent is to minimize wasted time spent debugging faults that impact the user experience.

