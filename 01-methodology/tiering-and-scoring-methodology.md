# Vendor Risk Tiering and Scoring Methodology

**Document Classification:** Internal / Security Program  
**Version:** 1.0  
**Date:** April 2026  
**Author:** Jelani D. Maitland  
**Context:** MedCaribe Health Group  
**Related Policy:** Vendor and Third-Party Risk Management Policy (POL-005)

---

## 1. Purpose

This document defines how MedCaribe Health Group classifies vendors into risk tiers and scores vendor security questionnaire responses. It provides the objective criteria that drive all vendor risk decisions, from assessment scope to review frequency.

---

## 2. Vendor Risk Tiering

### 2.1 Tiering Criteria

Every vendor that accesses MedCaribe data or provides technology services must be assigned a risk tier. The tier determines the assessment depth, contractual requirements, and review frequency.

Tiering is based on two factors: **data sensitivity** (what data does the vendor access or process?) and **service criticality** (what happens to MedCaribe's operations if this vendor fails?).

### 2.2 Tiering Matrix

| | Low Service Criticality | High Service Criticality |
|---|---|---|
| **Restricted / Confidential Data Access** | Tier 2 (Important) | Tier 1 (Critical) |
| **Internal / Public Data Only** | Tier 3 (Standard) | Tier 2 (Important) |
| **No Data Access** | Tier 3 (Standard) | Tier 3 (Standard) |

**Data sensitivity** is determined by the highest classification level of data the vendor accesses, using the four tiers from MedCaribe's Data Classification Policy (POL-004): Public, Internal, Confidential, Restricted.

**Service criticality** is High if MedCaribe cannot deliver clinical services or process billing without the vendor for more than 24 hours. All other vendors are Low criticality.

### 2.3 Tier Definitions

| Tier | Label | Criteria | Assessment | Review Cycle |
|------|-------|----------|------------|-------------|
| 1 | Critical | Accesses Restricted data AND/OR service failure halts clinical operations within 24 hours | Full questionnaire (45 questions). SOC 2 or equivalent audit report requested. Data processing agreement required. | Annual |
| 2 | Important | Accesses Confidential data OR supports (but does not enable) core operations | Abbreviated questionnaire (20 questions). Data processing agreement required where personal data is shared. | Every 2 years |
| 3 | Standard | No access to sensitive data. Non-critical services. | No formal assessment. Standard contract terms. | Only if scope changes |

### 2.4 MedCaribe Vendor Classification

| Vendor | Data Accessed | Criticality | Assigned Tier |
|--------|--------------|-------------|---------------|
| CloudMed EHR | Patient records, diagnoses, prescriptions, lab results (Restricted) | High: clinical ops stop without EHR | **Tier 1** |
| Microsoft (M365) | Business email, internal documents, some patient-adjacent data (Confidential) | High: email, Teams, file access all stop | **Tier 1** |
| QuickBooks (Intuit) | Financial records, salary data, vendor payments (Confidential) | Low: billing disrupted but clinical ops continue | **Tier 2** |
| Sagicor (Insurance) | Patient identity, policy numbers, diagnoses, claims (Restricted) | Low: claim processing delayed but care continues | **Tier 2** |
| Guardian Life (Insurance) | Patient identity, policy numbers, diagnoses, claims (Restricted) | Low: same as Sagicor | **Tier 2** |
| External Reference Labs | Patient samples, requisition data, results (Restricted) | Low: specialized tests delayed but routine care continues | **Tier 2** |
| Office Supply Vendors | Purchase orders only (Internal) | Low | **Tier 3** |
| Cleaning Services | No data access | Low | **Tier 3** |

---

## 3. Questionnaire Scoring Methodology

### 3.1 Response Options

Each questionnaire question uses a four-level response scale:

| Response | Score | Definition |
|----------|-------|------------|
| Fully Implemented | 3 | The control or practice is in place, documented, and consistently followed |
| Partially Implemented | 2 | The control exists but is inconsistent, undocumented, or has known gaps |
| Planned | 1 | The vendor has committed to implementing the control with a defined timeline |
| Not Implemented | 0 | The control does not exist and there is no plan to implement it |

### 3.2 Question Weighting

Not all questions carry equal weight. Questions are weighted by their impact on MedCaribe's risk:

| Weight | Label | Applied To | Multiplier |
|--------|-------|-----------|------------|
| Critical | Must-have controls | MFA, encryption, breach notification, backup and recovery, access control | x3 |
| High | Important controls | Patch management, logging, security training, incident response, data disposal | x2 |
| Standard | Good practices | Change management, physical security, business continuity, documentation | x1 |

### 3.3 Scoring Calculation

For each question:
**Question Score = Response Score (0-3) x Weight Multiplier (1-3)**

For the overall assessment:
**Vendor Score = Sum of All Question Scores / Maximum Possible Score x 100**

This produces a percentage that maps to a risk rating.

### 3.4 Risk Rating Thresholds

| Score Range | Rating | Meaning | Action |
|-------------|--------|---------|--------|
| 80-100% | Low Risk | Vendor meets or exceeds security expectations | Approve. Standard monitoring. |
| 60-79% | Medium Risk | Vendor has some gaps that should be addressed | Approve with conditions. Document gaps. Request remediation timeline. Review in 6 months. |
| 40-59% | High Risk | Significant security gaps exist | Escalate to Medical Director. Accept risk with documented justification OR require remediation before engagement OR seek alternative vendor. |
| 0-39% | Critical Risk | Vendor security is fundamentally inadequate | Do not approve without Medical Director sign-off and documented risk acceptance. Strongly consider alternative vendor. |

### 3.5 Risk Acceptance

Some vendor gaps may be accepted when the cost or disruption of switching vendors exceeds the risk, no alternative vendor exists in the market, or compensating controls at MedCaribe reduce the residual risk.

All risk acceptances must be documented with the specific gap being accepted, the business justification, compensating controls in place, the name of the person accepting the risk (Medical Director for Tier 1), and a review date (no longer than 12 months).

---

## 4. Assessment Process

### 4.1 New Vendors

Before engaging any Tier 1 or Tier 2 vendor:

1. Classify the vendor using the tiering matrix (Section 2)
2. Send the appropriate questionnaire (Tier 1: full, Tier 2: abbreviated)
3. Score the responses using the methodology in Section 3
4. Review any supporting documentation (SOC 2 reports, certifications, policies)
5. Document findings and risk rating
6. For Tier 1: present findings and recommendation to Medical Director for approval
7. For Tier 2: Operations Manager approves
8. Add vendor to the Vendor Risk Register

### 4.2 Existing Vendors

All existing Tier 1 and Tier 2 vendors must be assessed within 6 months of this framework's adoption. Priority order:

1. CloudMed EHR (Tier 1, highest data exposure, validated by Project 3 vendor breach scenario)
2. Microsoft M365 (Tier 1, but Microsoft provides publicly available SOC 2 and ISO 27001 reports)
3. Insurance portals (Tier 2, Restricted data but lower criticality)
4. QuickBooks / Intuit (Tier 2, Confidential data)
5. External reference labs (Tier 2, Restricted data)

### 4.3 Reassessment Triggers

Beyond the standard review cycle, reassessment is required when the vendor experiences a security incident, the vendor's services or data access scope changes, MedCaribe's data classification for the vendor changes, contract renewal is approaching, or the vendor changes ownership or undergoes significant organizational change.

---

## 5. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | April 2026 | J. Maitland | Initial methodology |

**Next Review:** April 2027 or upon significant change to vendor relationships.
