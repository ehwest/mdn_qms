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
# Risk and Hazard Management

The purpose of this chapter is to define the risk management process used by MDN LLC to document and maintain an ongoing process for identifying hazards associated with MDN medical devices, estimating and evaluating the associated risks, controlling these risks, and monitoring the effectiveness of the controls. 

It should be generally understood that ALL references to manufactured "device" or "devices" mentioned in the sections below are applicable to services delivered by software  operating on one or more compute environments operated by MDN.  MDN does not manufacture tangible devices, but rather is leveraging the FDA approach to define "software applications" as manufactured devices, subject to rules and regulations of devices, where possible.

This Quality Management System is designed to meet or exceed the applicable ISO standards for Quality Management Systems, and Risk Management standards found in the following references.

The plans and practices outlined in these references are believed to be entirely contained in the specific definitions, Plans, and Risk Assessment Activities described below the reference section.
If and/or when there is some difference in the references compared to to the QMS details following the references, the QMS documentation is authoritative and is used.


  1. [ISO 14971:2019](https://www.iso.org/standard/72704.html) ISO Medical Devices -- Application of risk management to medical devices. 
  2. [ISO 13485:2016](https://www.iso.org/standard/59752.html) ISO Medical Devices -- Quality Management Systems -- Requirements for regulatory purposes.
  3. [21 CFR Part 820, US FDA Quality System Regulation](https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfcfr/CFRSearch.cfm?CFRPart=820) -- FDA Code of Federal Regulations Title 21 -- Part 820 Quality System Regulation

## Definitions

 * Harm - Physical injury or damage to the health of people, or damage to property or the environment
 * Hazard - Potential source of harm
 * Hazardous Situation - Circumstance in which people, property, or the environment are exposed to one or more hazard(s)
 * Life-cycle – All phases in the life of a medical device, from the initial conception to final decommissioning and disposal
 * Post-production – Part of the life-cycle of the product after the design has been completed and medical device has been manufactured
 * Residual Risk – Risk remaining after risk control measures have been taken
 * Risk – Combination of the probability of occurrence of harm and the severity of that harm
 * Risk Analysis – Systematic use of available information to identify hazards and to estimate the risk
 * Risk Assessment – Overall process comprising a risk analysis and a risk evaluation
 * Risk Control – Process in which decisions are made and measures implemented by which risks are reduced to, or maintained within, specified levels
 * Risk Estimation – Process used to assign values to the probability of occurrence of harm and the severity of that harm
 * Risk Evaluation – Process of comparing the estimated risk against given risk criteria to determine the acceptability of the risk
 * Risk Management – Systematic application of management policies, procedures and practices to the tasks of analyzing, evaluating, controlling and monitoring risk
 * Risk Management File (RMF) – Set of records and other documents that are produced by risk management
 * Safety – Freedom from unacceptable risk
 * Senior Management – CEO and other senior executives
 * Severity – Measure of the possible consequences of a hazard
 * Use error – Act or omission of an act that results in a different medical device !response than intended by the manufacturer or expected by the user
 * Verification – Confirmation, through the provision of objective evidence, that specified requirements have been fulfilled

    
###Baselined Risks

It is assumed that all tasks have baseline risks. 
Baseline risks are documented on an MS Excel Spreadsheet stored in the software github repository.
New Baseline Risks are added iteratively. If a task or process does NOT indicate additional risks, then only the Baseline Risks are assumed.

on an MS Excel Spreadsheet stored in the MSN software github repository.
New Baseline Risks are added iteratively. If a task or process does NOT indicate additional risks, then only the Baseline Risks are assumed.
  
## Risk analysis occurs regularly and continuously as a part of all processes. If a task is determined to have risk(s), then those risk(s) are documented.

### Definitions of Severity Terms

| **Rating** | **Term** | **Description** | **Short example** |
| --- | --- | --- | --- |
| 5 | Catastrophic | Results in patient death. | Death due to hypoglycemia. |
| 4 | Critical | Results in permanent impairment or life-threatening injury. | Hypoglycemic coma. |
| 3 | Serious | Results in injury or impairment requiring professional medical intervention. | Hypoglycemic seizure or diabetic ketoacidosis requiring hospitalization. Serious injury due to hypoglycemia-induced fainting. |
| 2 | Minor | Results in temporary injury or impairment not requiring professional medical intervention. | Confusion or disorientation due to minor hypoglycemia. |
| 1 | Negligible | Inconvenience or temporary discomfort. | Feeling a little low, quickly recovering. |
| 0 | None | A bug or issue that has no chance of causing harm. | Minor user interface issue that will not cause misinterpretation of data. Bug found and fixed prior to delivery to production |


### Definition of &quot;Probability of Harm&quot; Terms

| **Rating** | **Term** | **Probability (P) of Occurrence of the Harm** **(not the bug)** | **Description for Clarity** |
| --- | --- | --- | --- |
| 5 | Frequent | P ≥ 0.1 | Likely to occur 1 in 10 times or more often. |
| 4 | Probable | .01 ≤ P \&lt; 0.1 | Likely to occur between (1 in 10) and (1 in 100) times. |
| 3 | Occasional | .0001 ≤ P \&lt; 0.01 | Likely to occur between (1 in 100) and (1 in 10,000) times. |
| 2 | Remote | .000001 ≤ P \&lt; 0.0001 | Likely to occur between (1 in 10,000) and (1 in 1,000,000) times. |
| 1 | Improbable | P ≤ 0.000001 | Likely to occur less frequently than 1 in a million times. |

Probability of a risk is determined by estimating the likelihood that the risk will manifest as a harm for any given use of MDN software. &quot;Use&quot; means an instance of using a MDN software for its intended use.

### Risk Rating

A Risk Rating is determined by multiplying the occurrence rating by the severity rating to obtain a result ranging from 1-25. Decisions about risk acceptability are based on the following table:


|**Severity**|**None**|**Negligible**|**Minor**|**Serious**|**Critical**|**Catastrophic**|
|----------|----------|----------|----------|----------|----------|----------|
| **Probability** | | | | | | |
| **Frequent** | 0 | 6 | 13 | 17 | 21 | 25 |
| **Probable** | 0 | 5 | 12 | 16 | 20 | 24 |
| **Occasional** | 0 | 4 | 8 | 15 | 19 | 23 |
| **Remote** | 0 | 2 | 7 | 14 | 18 | 22 |
| **Improbable** | 0 | 1 | 3 | 9 | 10 | 11 |


##3 Risk Management Procedures 

1. All software and medical devices have risks. MDN&#39;s risk management activities reduce risk.
2. Unless otherwise documented, all MDN software is assumed to have Baseline Risks, as defined below.
3. All risks, including Baseline Risks, are analyzed, estimated, evaluated and documented as described below.
4. Risk Management activities, including review of the Risk Management process, are iterative and continuous. There are no point-in-time &quot;Risk Acceptance&quot; gates.
5. MDN&#39;s risk management process follows the process identified in [ISO 14971 Recognized Consensus Standard](https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfStandards/detail.cfm?standard__identification_no=30596).
 6. MDN&#39;s CEO ensures that there are adequate resources for the risk management process and that these personnel are qualified for risk management with the knowledge and experience appropriate to the tasks assigned to them.

### Risk Management Plan and File

MDN has designed its own Risk Management Plan based on analysis of existing state of the art for software and medical device. We base our model on these tenets:
  
1. **Reduction** of risk through software iteration over time.
    
Processes that inhibit iteration cycles add risk. MDN uses agile design and development methodology, including verification and validation processes. The more quickly we can iterate on our software, the more quickly we can converge on high quality software that meets the user&#39;s needs while maintaining (or improving) software safety and efficacy.
    
2. **Comparison**  of risks and mitigations, including comparison to baseline risk of living with diabetes.
    
All software and medical devices contain risks and flaws, both known and unknown. Diabetes is also an inherently risky disease. Existence of a residual risk in MDN&#39;s software must be compared against the risk of unavailability of MDN software or other diabetes management software for a person living with diabetes.
    
MDN establishes a risk management plan for each medical device. This plan includes the scope of the risk management activities, assignment of responsibilities and authorities, criteria for risk acceptability, verification activities and activities related to the collection and review of production and post-production information.
    
This risk management plan, risk evaluation, implementation and verification of risk control measures, and the assessment of acceptability of any residual risks comprise the Risk Management File. The Risk Management File is an index with pointers to the required documentation.


### Risk Analysis

1. For each medical device, MDN documents the intended use and reasonably foreseeable misuse, as well as documenting qualitative and quantitative characteristics that could affect the safety of the medical device. 
A form "Device Characteristics" is used to document the results of this review.
  
2. Hazardous situation(s) are recorded after conducting an assessment of reasonably foreseeable sequences or combinations of events that can result in a hazardous situation.
  
3. The associated risk for each hazardous situation is estimated using available information or data. Risk estimation is based on assigning Severity and Probability to a given hazard. Severity and Probability are defined below.
  
4. For each identified risk, these questions are asked and the results are documented:
  
    A. What is the severity of this risk?
    
### Risk Acceptability

1. Risk levels 1, 2 and 3: Further risk reduction will be assessed. Once this risk has been reduced as far as possible, this risk is acceptable for users to continue using MDN software with these residual risks. For known risks that may have potential fixes or mitigations, the potential fix or mitigation should be documented so that it can be considered relative to future work during future prioritization.
2. Risk levels 4 through 11: Risk reductions must be considered and a mitigation plan must be documented and put in place. Once these risks have been reduced as far as possible, these risks are considered acceptable.
3. Risk levels 12 through 25: These risks must be reduced. The work must be prioritized and addressed ahead of other work on the same feature area. A mitigation plan must be documented and put in place. A communication plan to users must be documented and implemented. Prior to product release, risk must be reduced to an acceptable level or a Risk/Benefit analysis must be performed prior to product release for human use. If the medical benefits outweigh the overall residual risk, then the overall residual risk can be judged acceptable.

### Risk Evaluation

1. For each identified hazardous situation, MDN will decide whether the risk can be further reduced. Any requirement for risk reduction, or if none is required, is recorded in the risk analysis.
  
2. All risks shall be reduced as far as possible.
  
3. Risks will generally be categorized as Acceptable or Unacceptable. Any risks determined unacceptable require risk reduction prior to going to market.

### Risk Control
1. When risk reduction is required, risk control activities as described below will be performed.
2. In the event that risk reduction is necessary, risk control measures will be identified and documented. Risk control measures are applied in the following priority:
    - Safety by design (inherent) - eliminates hazard or hazardous situation via design feature
    - Protective measures - prevent or reduce likelihood of occurrence of hazard or hazardous situation
    - Information for safety - warnings, precautions, and/or information provided regarding hazard or hazardous situation
    
3. The risk control measures that are identified are verified and the effectiveness of the risk control measures, which may include validation activities, are documented accordingly.
  
4. Upon implementing the risk control measures, the residual risks are then evaluated according to the criteria established above. Generally, if the residual risk has a risk rating ≤11, then it is determined to be acceptable.
  
5. If residual risks are still determined to be unacceptable, additional risk controls will be identified and implemented.
  
6. For residual risks that have been reduced as low as possible, top management will decide which residual risks to disclose and what information for safety is necessary to include in the Instructions for Use in order to disclose those residual risks.
  
7. Following the residual risk evaluation, an assessment is made as to whether the medical benefits of the device outweigh the residual risks. Clinical evaluation of the product and any other relevant published clinical literature may be considered in making the determination. If the evaluation demonstrates that the medical benefits of the device do not outweigh the residual risks, the device is not released to production.
  
8. The risk control measures that have been implemented are also evaluated to determine if they have introduced any new hazards or hazardous situations and whether the estimated risks for previously identified hazardous situations are affected.
  
9. Once all risk control measures have been implemented, a review is performed to determine whether the risks from all identified hazardous situations have been considered.
  
### Evaluation of Overall Residual Risk Acceptability

1. After all the risk control measures have been implemented and verified, it will be determined whether the overall residual risk posed by the medical device has been reduced as low as possible using the criteria defined in the Risk Management Plan.
  
2. If the overall residual risk is not judged to be reduced as far as possible using the criteria established in the Risk Management Plan, then further data and literature may be gathered and reviewed to determine if the medical benefits of the intended use outweigh the overall residual risk. If the evidence supports that the benefits outweigh the overall residual risks, the the overall residual risk can be judged to be as low as possible. Otherwise, the overall residual risk remains unacceptable.
  
3. Risk Management Report:  Prior to release, MDN reviews the risk management process to ensure that it has been appropriately implemented and that the overall residual risk is accepted.
  
4. These results will be documented in the Risk Management Report and included in the Risk Management File.

5. Production and Post-production Information

On an iterative, ongoing basis, complaints, bug reports and other user feedback are compiled and evaluated per chapter 3 "Corrective and Preventive Action" and chapter 5 "Complaint Handling"

__Notes on "As Far As Possible"__

The term and understanding of the phrase for reducing risk "As Far As Possible" is hereby understood to be a holistic definition that balances unit cost, business goals, the incremental benefits and impact for improving risk.  What is "possible" is defined in the context of a specific and contemporary
"willingess to pay" for the realization of the "possible."   If there is no one willing to pay for the possible then, by definition, it is not possible.

