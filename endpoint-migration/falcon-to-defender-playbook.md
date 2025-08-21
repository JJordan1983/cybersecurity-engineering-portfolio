
---

## 🔑 Case Study Summaries

### 1. Endpoint Migration — Falcon → Microsoft Defender
**File:** [`endpoint-migration/falcon-to-defender-playbook.md`](./endpoint-migration/falcon-to-defender-playbook.md)

- **Scope:** Transition from CrowdStrike Falcon to Microsoft Defender for Endpoint, Identity, and Office 365.  
- **Phases:** Assessment → Pilot → Execution → Hardening → Validation.  
- **Policy Baselines:** ASR (Attack Surface Reduction), EDR in block mode, Tamper Protection, Network Protection.  
- **Validation:** KQL queries in Sentinel to confirm detection parity and incident creation.  
- **Outcomes:** Zero downtime, 30% uplift in detection coverage, 100% compliance with DISA STIG/RMF.  
- **Rollback:** Documented reinstall and policy reversion procedure.

---

### 2. Vulnerability Management — ACAS Cadence
**File:** [`vuln-management/acas-vuln-management-cadence.md`](./vuln-management/acas-vuln-management-cadence.md)

- **Scope:** Enterprise vulnerability management using Tenable Nessus / SecurityCenter (ACAS).  
- **Cadence:** Weekly (HVAs), Monthly (enterprise), Event-driven (zero-day/new builds).  
- **Prioritization:** CVSS + CISA KEV + mission impact + exploitability.  
- **Remediation SLAs:** 15 days (Critical), 30 days (High), 90 days (Medium).  
- **POA&M Workflow:** Lifecycle tracking (Open → Mitigated → Closed) with template.  
- **Outcomes:** 25% reduction in criticals, 100% SLA compliance, zero major audit findings.

---

## 📊 Supporting Artifact

- **POA&M Tracking Template** → [`vuln-management/poam-tracking-template.csv`](./vuln-management/poam-tracking-template.csv)  
A reusable template for tracking vulnerabilities, remediation actions, owners, and audit status.

---

## 🛡️ Security & Compliance Alignment

These playbooks reflect alignment with:
- **Frameworks:** NIST SP 800-53, RMF, DISA STIGs  
- **Mandates:** DoD vulnerability management timelines, CISA KEV advisories  
- **Tools:** Microsoft Defender, Microsoft Sentinel, Tenable Nessus (ACAS)  

---

## 👤 Author

**Jeanette Jordan**  
DoD Secret Clearance | CISM, CEH, Security+  
Cybersecurity Engineer & ISSM — specializing in **tool integration, compliance alignment, and mission resilience**.  

📍 Stafford, VA  
📧 JeanetteD_Jordan@outlook.com  
🔗 [LinkedIn](https://www.linkedin.com/in/jeanettejordan)  

---

## 📜 License

Released under the [MIT License](./LICENSE).  
Use, adapt, and build upon these materials freely with attribution.

---
