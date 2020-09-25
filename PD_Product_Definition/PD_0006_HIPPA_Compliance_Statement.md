---
repository: "github.com/ehwest/mdn_qms"
folder: "PD"
title: "PD_0001_T1PAL_PRODUCT_REQUIREMENTS.md"
document_id: "PD_0001"
authors:
- github.com/ehwest
approvers:
- github.com/bewest
revision: "05"
approval_date: "2020-08-24"
effective_date: "2020-08-24"
description: "T1Pal Product Requirements"
---


## T1Pal System Requirements

This document conveys the general requirements of the T1Pal service product.
T1Pal is a service that is provided by executing software applications that 
run on compute servers operated by
Medical Data Networks, LLC.   To use the software, consumers must apply for a monthly subscription-based
access to the server complex to receive the benefits of the service.
Subscribers access the service by using any of the following devices:
+ iPhone cell phone with an interent data service plan
+ Androidcell phone with an internet  data service plan
+ desktop or laptop PC with Firefox browser and Internet connectivity

T1Pal software and emergent services are expected to fit the FDA's
definition of SaMD.
[FDA Definition of Software as a Medical Device[(https://www.fda.gov/media/119722/download)
"Software as a Medical Device" (SaMD) is defined as software intended to be
used for one or more medical purposes that perform these purposes without being part of a hardware
medical device.

### REQ_1000
T1Pal is secoondary display of data from an "Integrated Continuous Glucose Monitoring System" intended to automatically display
past and present measures of selected bodily fluids frequently.   

### REQ_1010
T1Pal is a "secondary display" of data that is securely obtained and delivered by electronic messages securely transmitted from other devices, distinct from T1Pal services and operations.
These other devices include:  
+ insulin dosing systems, 
+ integrated Continuous Glucose Monitoring systems (iCGM).

### REQ_1020
T1Pal provides a display of data that combines data from multiple sources and displays a consolidated view of the data such that the timing of reports of bodily fluids are synchronized in time.
Sources of data displayed on the T1Pal system are required to comply with agreed data communications requirements.  
Products that do comply with T1Pal system agrements include:  
+ Dexcom G4, G5 products that use the Dexcom Share Service phone-based application and bluetooth bridge.
+ Dexcom's G6 continuous glucose monitoring system, using Dexcom Follow service. 
+ Insulet's Omnipod Insulin Management system, 
+ MiniMed insulin pump system from Medtronic, 
+ Medtronic's Guardian Connect CGM system.


### REQ_1030
T1Pal as a service that is accessed using an Internet connection. Excluding individual subscriber internet impairments, T1Pal has no scheduled downtime, and expectes to operate 24 x 7 x 365 nonstop. 
The design of T1Pal provides for more than 60 minutes of unavailability per year, for all causes.  
Subscribers will loose no data once such data has been delivered by remote systems to the T1Pal server complex.
Subscriber data will be archived for five years after such data is first delivered.

### REQ_1040
T1Pal enforces compliance to HIPAA privacy requirements.

### REQ_1050
T1Pal provides for the subscriber to generate secure internet service links that, when transferred to other individuals, enables them to temporarily gain access to view the T1Pal reports.
These links become expired under control of the subscriber.

### REQ_1060
T1Pal software shall operate in such a way that new features may be added, existing bugs may be fixed, and performance may be improved without pausing services delivered to subscribers.

### REQ_1070
T1Pal software shall operate in such a way that subscribers may access assistance and report apparant bugs at any time.





## Responsibilities

1. The CEO and VP-level employees are responsible for overseeing and maintaining this standard operating procedure and for assuring that all employees are trained in its requirements.
2. It is the responsibility of all employees, contractors and departments at Medical Data Networks to adhere to this procedure.
