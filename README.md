# Third-Party Vendor Risk Assessment Framework

## Practical Vendor Risk Management for a Caribbean Healthcare Provider

**Context:** MedCaribe Health Group, 55-person private healthcare provider, Trinidad and Tobago  
**Regulatory Basis:** Trinidad and Tobago Data Protection Act (2011)  
**Author:** Jelani D. Maitland  
**Date:** April 2026  
**Related Projects:**  
- [Project 1: MedCaribe Security Program](https://github.com/jelanidm/medcaribe-security-program)  
- [Project 2: CIS Controls v8 IG1 to M365 Mapping](https://github.com/jelanidm/m365-cis-controls-mapping)  
- [Project 3: Tabletop Exercise Kit](https://github.com/jelanidm/tabletop-exercise-kit)

---

## Overview

This repository provides a complete, ready-to-use vendor risk assessment framework for MedCaribe Health Group. It operationalizes the Vendor and Third-Party Risk Management Policy (POL-005) created in Project 1 by providing the actual tools needed to assess, score, and track vendor security risk.

The framework is designed for organizations that have never formally assessed their vendors before. It assumes limited GRC resources and prioritizes simplicity over complexity.

---

## Why Vendor Risk Management?

MedCaribe's patient data flows through multiple third-party systems every day: the cloud EHR stores 12,000+ patient records on US-based servers, insurance portals process claims containing diagnoses and policy numbers, and external labs receive patient samples and results.

Under the Trinidad and Tobago Data Protection Act, MedCaribe is responsible for the protection of personal data regardless of whether a third party processes it. If CloudMed gets breached (as simulated in Project 3, Scenario 3), MedCaribe bears the regulatory liability.

Yet prior to this framework, MedCaribe had never assessed a single vendor's security practices, had no security clauses in vendor contracts, and had no process for tracking vendor risk over time.

---

## What This Framework Includes

**Tiering and Scoring Methodology** - How to classify vendors into risk tiers based on data access and service criticality, and how to score questionnaire responses objectively.

**Two Questionnaires** - A full questionnaire (45 questions) for Tier 1 critical vendors and an abbreviated questionnaire (20 questions) for Tier 2 important vendors. Both are structured by security domain.

**Sample Completed Assessment** - A worked example showing CloudMed EHR assessed using the Tier 1 questionnaire, with scored responses, identified gaps, and risk-accepted items. This demonstrates what a real assessment looks like.

**Vendor Risk Register** - A tracking document for all Tier 1 and Tier 2 vendors showing risk tier, assessment status, key findings, and review dates.

---

## Repository Structure

```
vendor-risk-assessment-framework/
├── README.md
├── 01-methodology/
│   └── tiering-and-scoring-methodology.md
├── 02-questionnaires/
│   ├── tier-1-full-questionnaire.md
│   └── tier-2-abbreviated-questionnaire.md
├── 03-sample-assessment/
│   └── sample-cloudmed-ehr-assessment.md
├── 04-tracking/
│   └── vendor-risk-register.md
└── pdf-versions/
    └── (all documents exported as PDF)
```

---

## Connection to the MedCaribe Portfolio

| Project | What It Built | How Project 4 Connects |
|---------|--------------|----------------------|
| Project 1 | Vendor Risk Policy (POL-005) | This framework provides the tools POL-005 requires: questionnaires, tiering, and tracking |
| Project 2 | CIS Controls mapping | CIS Control 15 (Service Provider Management) is directly implemented by this framework |
| Project 3 | Vendor Breach TTX (Scenario 3) | The exercise exposed gaps that this framework prevents: no vendor assessment, no contract clauses, no backup verification |

---

## About the Author

Jelani D. Maitland is a cybersecurity professional based in Trinidad and Tobago, holding CySA+, Security+, SC-200, and Fortinet FCA certifications. He specializes in security operations, governance, and risk management for small and midsize organizations in the Caribbean.

- [LinkedIn](https://linkedin.com/in/jelanidm)
- [GitHub](https://github.com/jelanidm)

---

## License

This project is shared under the [MIT License](LICENSE). You are free to use, modify, and distribute these materials with attribution.
