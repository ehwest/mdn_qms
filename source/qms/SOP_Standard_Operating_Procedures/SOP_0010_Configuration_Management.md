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
# Configuration Management

## Preferred Use over Command Lines
The use of configuration files is intended to eliminate and/or reduce the use of command line functions to control and configure the components of T1Pal operations.
The reduction and/or elimination of command-line functions is a key to automating complex tasks that require the attention of highly skilled associates at inconvenient hours.

## Scope of Use
Configuration files shall be used in every software design used and developed by Medical Data Networks LLC (MDN).  In addition, all such configuration files shall be managed as code within the github software repository.

Configuration files will be read upon the deployment and/or restart of new software components.  
Configuration files shall themselves be versioned (refer to Semantic Versioning guidelines).
