# Tier 1 Vendor Security Questionnaire

**For:** Critical vendors (store Restricted data and/or provide services essential to clinical operations)  
**Questions:** 45  
**Estimated Completion Time:** 60-90 minutes  
**Version:** 1.0 | April 2026

---

## Instructions for Vendor

Please answer each question by selecting one of the following:

- **Fully Implemented (3):** Control is in place, documented, and consistently followed
- **Partially Implemented (2):** Control exists but is inconsistent, undocumented, or has gaps
- **Planned (1):** Committed to implementing with a defined timeline
- **Not Implemented (0):** Control does not exist and no plan to implement

Where requested, provide brief supporting evidence or documentation references. If a question is not applicable to your environment, mark N/A and explain.

---

## Vendor Information

| Field | Response |
|-------|----------|
| Vendor Name | |
| Primary Contact Name | |
| Contact Email | |
| Contact Phone | |
| Services Provided to MedCaribe | |
| Data Types Accessed / Processed | |
| Data Hosting Location(s) | |
| Date Questionnaire Completed | |
| Completed By (Name and Title) | |

---

## Domain 1: Organizational Security (5 questions)

| # | Question | Weight | Response | Evidence / Notes |
|---|----------|--------|----------|-----------------|
| 1.1 | Does your organization have a documented information security policy that is reviewed at least annually? | Standard | | |
| 1.2 | Is there a designated individual or team responsible for information security (e.g., CISO, Security Manager)? | Standard | | |
| 1.3 | Does your organization hold any current security certifications (e.g., SOC 2 Type II, ISO 27001)? If yes, please provide the most recent report or certificate. | High | | |
| 1.4 | Do you carry cyber liability insurance? If yes, what is the coverage limit? | Standard | | |
| 1.5 | Do you have a documented risk management process that includes regular risk assessments? | High | | |

---

## Domain 2: Access Control (7 questions)

| # | Question | Weight | Response | Evidence / Notes |
|---|----------|--------|----------|-----------------|
| 2.1 | Is multi-factor authentication (MFA) required for all employees accessing systems that store or process MedCaribe data? | Critical | | |
| 2.2 | Is access to MedCaribe data restricted to employees with a documented business need (principle of least privilege)? | Critical | | |
| 2.3 | Do you have a formal process for granting, modifying, and revoking user access? | High | | |
| 2.4 | Are accounts disabled within 24 hours of employee departure? | High | | |
| 2.5 | Are administrative and privileged accounts separated from daily-use accounts? | High | | |
| 2.6 | Do you conduct periodic access reviews (at least quarterly) to verify access appropriateness? | Standard | | |
| 2.7 | Are passwords required to meet minimum complexity standards (12+ characters, complexity requirements)? | High | | |

---

## Domain 3: Data Protection (8 questions)

| # | Question | Weight | Response | Evidence / Notes |
|---|----------|--------|----------|-----------------|
| 3.1 | Is MedCaribe data encrypted at rest using industry-standard encryption (AES-256 or equivalent)? | Critical | | |
| 3.2 | Is MedCaribe data encrypted in transit using TLS 1.2 or higher? | Critical | | |
| 3.3 | Do you have a documented data classification policy? | Standard | | |
| 3.4 | Is MedCaribe data logically separated from other clients' data in your environment? | Critical | | |
| 3.5 | Do you have documented data retention and disposal procedures? | High | | |
| 3.6 | Upon contract termination, can you return all MedCaribe data and certify deletion of all copies within 30 days? | Critical | | |
| 3.7 | Do you process or store MedCaribe data outside of the country where the service is primarily provided? If yes, in which countries? | High | | |
| 3.8 | Do you have documented procedures to prevent unauthorized data exfiltration (DLP controls)? | Standard | | |

---

## Domain 4: Infrastructure and Network Security (5 questions)

| # | Question | Weight | Response | Evidence / Notes |
|---|----------|--------|----------|-----------------|
| 4.1 | Do you perform regular vulnerability scanning (at least quarterly) on systems that store or process MedCaribe data? | High | | |
| 4.2 | Do you perform penetration testing at least annually on customer-facing systems? | High | | |
| 4.3 | Is your network segmented such that a compromise in one area does not provide direct access to MedCaribe data? | High | | |
| 4.4 | Do you have an intrusion detection or intrusion prevention system (IDS/IPS) monitoring your environment? | Standard | | |
| 4.5 | Do you maintain a firewall between the internet and systems storing MedCaribe data? | Standard | | |

---

## Domain 5: Endpoint and Application Security (4 questions)

| # | Question | Weight | Response | Evidence / Notes |
|---|----------|--------|----------|-----------------|
| 5.1 | Do all endpoints accessing MedCaribe data have anti-malware software with automatic signature updates? | High | | |
| 5.2 | Do you have a documented patch management process that applies critical patches within 30 days of release? | High | | |
| 5.3 | Do you perform secure code reviews or application security testing on software that processes MedCaribe data? | Standard | | |
| 5.4 | Are endpoints that access MedCaribe data encrypted (full disk encryption)? | High | | |

---

## Domain 6: Backup and Recovery (5 questions)

| # | Question | Weight | Response | Evidence / Notes |
|---|----------|--------|----------|-----------------|
| 6.1 | Do you perform automated backups of MedCaribe data? If yes, how frequently? | Critical | | |
| 6.2 | Are backups stored in a location separate from the primary data environment? | Critical | | |
| 6.3 | Are backups encrypted? | High | | |
| 6.4 | Do you test backup restoration at least annually? When was the last successful test? | Critical | | |
| 6.5 | What is your committed Recovery Time Objective (RTO) and Recovery Point Objective (RPO) for MedCaribe's data? | Critical | | |

---

## Domain 7: Incident Response (5 questions)

| # | Question | Weight | Response | Evidence / Notes |
|---|----------|--------|----------|-----------------|
| 7.1 | Do you have a documented incident response plan? | High | | |
| 7.2 | In the event of a security incident affecting MedCaribe data, within what timeframe will you notify MedCaribe? | Critical | | |
| 7.3 | Do you conduct incident response exercises (tabletop or simulated) at least annually? | Standard | | |
| 7.4 | Do you have a dedicated incident response team or access to external IR support? | Standard | | |
| 7.5 | Will you provide MedCaribe with a detailed incident report including root cause analysis, affected data, and remediation steps following any incident? | High | | |

---

## Domain 8: Logging and Monitoring (3 questions)

| # | Question | Weight | Response | Evidence / Notes |
|---|----------|--------|----------|-----------------|
| 8.1 | Do you maintain audit logs of access to MedCaribe data, including user, timestamp, and action? | High | | |
| 8.2 | How long are audit logs retained? | Standard | | |
| 8.3 | Do you have 24/7 monitoring for security events on systems storing MedCaribe data? | Standard | | |

---

## Domain 9: Subcontractors and Fourth Parties (3 questions)

| # | Question | Weight | Response | Evidence / Notes |
|---|----------|--------|----------|-----------------|
| 9.1 | Do any subcontractors or fourth parties have access to MedCaribe data? If yes, please identify them. | High | | |
| 9.2 | Do you assess the security practices of subcontractors who access MedCaribe data? | High | | |
| 9.3 | Will you notify MedCaribe before engaging any new subcontractor who will access MedCaribe data? | High | | |

---

## Scoring Summary (Completed by MedCaribe)

| Domain | Max Score | Vendor Score | % |
|--------|-----------|-------------|---|
| 1. Organizational Security | | | |
| 2. Access Control | | | |
| 3. Data Protection | | | |
| 4. Infrastructure Security | | | |
| 5. Endpoint/App Security | | | |
| 6. Backup and Recovery | | | |
| 7. Incident Response | | | |
| 8. Logging and Monitoring | | | |
| 9. Subcontractors | | | |
| **Overall** | | | |

**Risk Rating:** Low / Medium / High / Critical

**Assessed By:** _______________  **Date:** _______________

---

## Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | April 2026 | J. Maitland | Initial questionnaire |
