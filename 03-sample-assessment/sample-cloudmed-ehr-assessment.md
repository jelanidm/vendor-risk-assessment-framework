# Sample Completed Assessment: CloudMed EHR

**Vendor:** CloudMed Health Systems Inc.  
**Tier:** 1 (Critical)  
**Assessed By:** J. Maitland, MedCaribe Health Group  
**Assessment Date:** April 2026  
**Questionnaire Used:** Tier 1 Full Questionnaire (45 questions)

---

## 1. Vendor Profile

| Field | Detail |
|-------|--------|
| Vendor Name | CloudMed Health Systems Inc. |
| Service Provided | Cloud-based Electronic Health Records (EHR) platform |
| Data Accessed | Patient demographics, medical history, diagnoses, prescriptions, lab results, appointment scheduling, insurance information |
| Data Classification | Restricted (highest tier per POL-004) |
| Data Hosting Location | United States (Virginia data center) |
| Service Criticality | High: clinical operations at all four MedCaribe locations stop without EHR access |
| Assigned Tier | Tier 1 (Critical) |
| MedCaribe Records Stored | Approximately 12,000 patient records over 5 years |

---

## 2. Assessment Summary

| Metric | Result |
|--------|--------|
| Questions Answered | 43 of 45 (2 marked N/A by vendor) |
| Overall Score | 67% |
| Risk Rating | **Medium Risk** |
| Critical-Weight Questions Passed (3/3) | 7 of 12 (58%) |
| Key Gaps Identified | 4 |
| Risk Acceptances Required | 1 |

---

## 3. Scoring by Domain

| Domain | Questions | Score | Max | % | Rating |
|--------|-----------|-------|-----|---|--------|
| 1. Organizational Security | 5 | 28 | 33 | 85% | Low Risk |
| 2. Access Control | 7 | 43 | 57 | 75% | Medium Risk |
| 3. Data Protection | 8 | 49 | 66 | 74% | Medium Risk |
| 4. Infrastructure Security | 5 | 24 | 33 | 73% | Medium Risk |
| 5. Endpoint/App Security | 4 | 19 | 24 | 79% | Medium Risk |
| 6. Backup and Recovery | 5 | 27 | 45 | 60% | Medium Risk |
| 7. Incident Response | 5 | 24 | 33 | 73% | Medium Risk |
| 8. Logging and Monitoring | 3 | 12 | 15 | 80% | Low Risk |
| 9. Subcontractors | 3 | 12 | 18 | 67% | Medium Risk |
| **Overall** | **45** | **238** | **324** | **67%** | **Medium Risk** |

---

## 4. Strengths Identified

**Organizational Security (85%):** CloudMed holds a current SOC 2 Type II report (dated October 2025) and has a designated Chief Information Security Officer. They carry USD $5M in cyber liability insurance. Their information security policy is reviewed annually.

**Logging and Monitoring (80%):** CloudMed maintains detailed audit logs of all access to patient data with a 12-month retention period. They operate a 24/7 Security Operations Center for their hosted infrastructure.

**Encryption:** Data is encrypted at rest (AES-256) and in transit (TLS 1.3). These are Critical-weight questions and both received full scores.

---

## 5. Key Gaps Identified

### Gap 1: Backup Restoration Testing Not Current

| Field | Detail |
|-------|--------|
| Domain | Backup and Recovery |
| Question | 6.4: Do you test backup restoration at least annually? |
| Response | Partially Implemented |
| Detail | CloudMed stated they perform backup tests "periodically" but could not confirm the date of the last successful full restoration test. Their response referenced a test from 18 months ago. |
| Weight | Critical |
| Impact | If backups are not tested, there is no guarantee data can be recovered after a ransomware attack or system failure. This was the exact scenario tested in Project 3 (TTX Scenario 3). |
| Recommendation | Request CloudMed perform a documented restoration test within 90 days and provide MedCaribe with the results. Include annual restoration test as a contractual requirement at next renewal. |
| Risk Level | High |

### Gap 2: Breach Notification Timeline Not Contractually Defined

| Field | Detail |
|-------|--------|
| Domain | Incident Response |
| Question | 7.2: Within what timeframe will you notify MedCaribe of a security incident? |
| Response | Partially Implemented |
| Detail | CloudMed stated they "aim to notify affected clients within 72 hours of confirming an incident." However, this is a stated goal, not a contractual commitment. The current MedCaribe-CloudMed contract contains no breach notification clause. |
| Weight | Critical |
| Impact | Without a contractual notification timeline, MedCaribe has no enforceable right to timely notification. The DPA requires MedCaribe to notify the Information Commissioner, which requires knowing about the breach first. |
| Recommendation | Add a contractual clause requiring notification within 48 hours of incident discovery (not confirmation). This aligns with the standard in POL-005. |
| Risk Level | High |

### Gap 3: No Subcontractor Notification Process

| Field | Detail |
|-------|--------|
| Domain | Subcontractors |
| Question | 9.3: Will you notify MedCaribe before engaging new subcontractors who access MedCaribe data? |
| Response | Not Implemented |
| Detail | CloudMed uses subcontractors for infrastructure management (AWS hosting) and customer support. They do not currently notify clients when new subcontractors are engaged. |
| Weight | High |
| Impact | A new subcontractor with access to MedCaribe data introduces fourth-party risk that MedCaribe cannot assess or monitor if not informed. |
| Recommendation | Request contractual clause requiring 30-day advance notification of new subcontractors who will access MedCaribe data, with the right to object. |
| Risk Level | Medium |

### Gap 4: Cross-Border Data Transfer Compliance

| Field | Detail |
|-------|--------|
| Domain | Data Protection |
| Question | 3.7: Do you process data outside the primary service country? |
| Response | Fully Implemented (the vendor was transparent) |
| Detail | CloudMed confirmed all MedCaribe data is stored in the US (Virginia). While they were transparent about this, MedCaribe has not completed the cross-border transfer assessment required by the Data Protection Act Section 6(l) to verify that comparable safeguards exist in the receiving jurisdiction. |
| Weight | High |
| Impact | MedCaribe is potentially non-compliant with the DPA for transferring patient data to the US without a documented safeguard assessment. This is a MedCaribe responsibility, not a CloudMed gap. |
| Recommendation | Complete a cross-border transfer assessment for the US jurisdiction. Review whether CloudMed's SOC 2 report and DPA provisions provide comparable safeguards. Document the assessment and conclusion. |
| Risk Level | Medium (MedCaribe-side action) |

---

## 6. Risk Acceptance

### Accepted Risk: Recovery Point Objective (RPO)

| Field | Detail |
|-------|--------|
| Question | 6.5: What is your committed RTO and RPO? |
| Vendor Response | RTO: 24 hours. RPO: 4 hours for database, 24 hours for document storage. |
| Gap | The 4-hour RPO means up to 4 hours of patient data could be lost in a recovery scenario. For a healthcare provider processing appointments, prescriptions, and lab results continuously, this represents potential loss of clinical data. |
| Acceptance Justification | No EHR vendor in the Caribbean market offers a shorter RPO at MedCaribe's current budget. The 4-hour RPO is industry-standard for this tier of cloud EHR product. Implementing a shorter RPO would require a significantly higher licensing tier. |
| Compensating Control | MedCaribe will implement a daily export of critical patient summary data to a separate secure storage location (manual process until automated tooling is budgeted). |
| Accepted By | Dr. A. Dorian, Medical Director |
| Review Date | October 2026 (6-month review) |

---

## 7. Action Items

| # | Action | Owner | Target Date | Status |
|---|--------|-------|-------------|--------|
| 1 | Request CloudMed perform documented backup restoration test | Ops Manager | 90 days | Not Started |
| 2 | Add 48-hour breach notification clause to CloudMed contract | Ops Manager + Medical Director | Next contract renewal | Not Started |
| 3 | Add subcontractor notification clause to CloudMed contract | Ops Manager | Next contract renewal | Not Started |
| 4 | Complete cross-border transfer assessment for US jurisdiction | Ops Manager | 60 days | Not Started |
| 5 | Implement daily patient data summary export (compensating control) | IT Admin | 30 days | Not Started |
| 6 | Schedule reassessment of CloudMed | Ops Manager | April 2027 | Scheduled |

---

## 8. Conclusion and Recommendation

CloudMed scores at 67% overall, placing them in the **Medium Risk** category. They demonstrate solid organizational security practices and maintain a current SOC 2 Type II report. However, four gaps require attention, particularly around backup restoration testing and contractual breach notification timelines.

**Recommendation: Approve with conditions.** Continue the relationship with CloudMed subject to the action items above being completed within their target timelines. The Medical Director has accepted the RPO risk with a compensating control.

This assessment should be reassessed in 12 months (April 2027) or immediately if CloudMed experiences a security incident.

---

## Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | April 2026 | J. Maitland | Initial assessment |
