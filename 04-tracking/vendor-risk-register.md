# MedCaribe Health Group - Vendor Risk Register

**Document Classification:** Confidential / Internal  
**Version:** 1.0  
**Date:** April 2026  
**Owner:** Operations Manager  
**Review Cycle:** Quarterly

---

## 1. Purpose

This register tracks all Tier 1 and Tier 2 vendors, their risk tier, assessment status, key findings, and review dates. It is the operational companion to the Vendor Risk Policy (POL-005) and the tiering methodology.

---

## 2. Tier 1 Vendors (Critical)

| Vendor | Service | Data Classification | Assessment Status | Risk Rating | Key Findings | Next Review |
|--------|---------|--------------------|--------------------|-------------|-------------|-------------|
| CloudMed Health Systems | Cloud EHR (patient records, scheduling, prescriptions) | Restricted | Completed April 2026 | Medium (67%) | 4 gaps: backup test not current, no contractual breach notification timeline, no subcontractor notification, cross-border transfer assessment needed | April 2027 |
| Microsoft (M365) | Email, files, identity, device management, endpoint security | Confidential | Pending | Expected: Low | Microsoft provides publicly available SOC 2 Type II and ISO 27001. Review of Microsoft DPA and service terms pending. | Assess by June 2026 |

---

## 3. Tier 2 Vendors (Important)

| Vendor | Service | Data Classification | Assessment Status | Risk Rating | Key Findings | Next Review |
|--------|---------|--------------------|--------------------|-------------|-------------|-------------|
| Sagicor (Insurance) | Insurance claim submission and tracking | Restricted | Not Started | TBD | Receives patient identity, policy numbers, diagnoses, claim amounts. Uses web portal with vendor-managed authentication. | Assess by August 2026 |
| Guardian Life (Insurance) | Insurance claim submission and tracking | Restricted | Not Started | TBD | Same data profile as Sagicor. Separate portal, separate credentials. | Assess by August 2026 |
| Intuit (QuickBooks Online) | Accounting, invoicing, payroll | Confidential | Not Started | TBD | Financial records, salary data, vendor payment information. US-hosted SaaS. | Assess by September 2026 |
| External Reference Labs | Specialized laboratory testing | Restricted | Not Started | TBD | Receives patient samples, requisition forms, returns lab results. Mix of portal and email communication. | Assess by September 2026 |

---

## 4. Tier 3 Vendors (Standard)

Tier 3 vendors do not require formal assessment. They are listed here for completeness.

| Vendor | Service | Data Access | Notes |
|--------|---------|------------|-------|
| Office supply vendors | Stationery, printer supplies | Purchase orders (Internal) | No sensitive data. Standard contract terms. |
| Cleaning services | Facility cleaning | None | No data access. Physical access to premises only. |
| Medical equipment suppliers | Clinical equipment, consumables | Purchase orders (Internal) | No patient or financial data. |
| ISP providers (per location) | Internet connectivity | Network traffic transits their infrastructure | Consider as Tier 2 if implementing DNS filtering through ISP. Currently Tier 3. |

---

## 5. Assessment Schedule

| Quarter | Vendors to Assess | Priority Rationale |
|---------|-------------------|-------------------|
| Q2 2026 (Apr-Jun) | CloudMed (done), Microsoft M365 | Tier 1 vendors assessed first |
| Q3 2026 (Jul-Sep) | Sagicor, Guardian Life, QuickBooks, External Labs | Tier 2 vendors with Restricted data before those with Confidential data |
| Q4 2026 (Oct-Dec) | Any new vendors onboarded during the year | Catch-up quarter |
| Q1 2027 (Jan-Mar) | Annual review of Tier 1 vendors (CloudMed, Microsoft) | Annual reassessment cycle begins |

---

## 6. Risk Acceptances Log

| Vendor | Gap Accepted | Justification | Compensating Control | Accepted By | Accepted Date | Review Date |
|--------|-------------|---------------|---------------------|-------------|---------------|-------------|
| CloudMed | 4-hour RPO for database | No vendor in market offers shorter RPO at current budget | Daily patient summary export to separate storage | Dr. A. Dorian | April 2026 | October 2026 |

---

## 7. Open Action Items

| # | Vendor | Action | Owner | Target Date | Status |
|---|--------|--------|-------|-------------|--------|
| 1 | CloudMed | Request documented backup restoration test | Ops Manager | July 2026 | Not Started |
| 2 | CloudMed | Add 48-hour breach notification clause at contract renewal | Ops Manager | At renewal | Not Started |
| 3 | CloudMed | Add subcontractor notification clause at contract renewal | Ops Manager | At renewal | Not Started |
| 4 | All vendors | Complete cross-border transfer assessment for US-hosted services | Ops Manager | June 2026 | Not Started |
| 5 | Microsoft | Review Microsoft DPA and SOC 2 report | IT Admin | June 2026 | Not Started |
| 6 | Sagicor | Send Tier 2 questionnaire | Ops Manager | July 2026 | Not Started |
| 7 | Guardian Life | Send Tier 2 questionnaire | Ops Manager | July 2026 | Not Started |
| 8 | QuickBooks | Send Tier 2 questionnaire | Ops Manager | August 2026 | Not Started |

---

## 8. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | April 2026 | J. Maitland | Initial register with CloudMed assessment complete |

**Next Review:** July 2026 (quarterly) or when any vendor assessment is completed.
