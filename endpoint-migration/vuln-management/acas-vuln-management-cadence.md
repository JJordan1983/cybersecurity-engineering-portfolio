# ACAS Vulnerability Management Cadence

This playbook documents a standardized cadence for **Assured Compliance Assessment Solution (ACAS)** vulnerability scanning and remediation tracking in a DoD-style environment.  
It ensures continuous visibility, risk-based remediation, and compliance with **DISA STIGs, NIST SP 800-53, RMF**, and DoD timelines.  

---

## 🎯 Objectives
- Establish consistent scanning intervals for enterprise and high-value systems.  
- Prioritize vulnerabilities based on mission risk, not just CVSS score.  
- Enforce remediation timelines aligned with DoD/agency policy.  
- Track remediation and exceptions via a structured POA&M process.  
- Provide metrics to leadership and auditors for compliance assurance.  

---

## 📌 Scan Strategy
1. **Weekly**  
   - Credentialed scans for High-Value Assets (HVAs) and mission-critical systems.  

2. **Monthly**  
   - Full enterprise scans (authenticated where possible).  
   - Non-credentialed scans for shadow IT discovery.  

3. **Event-Driven**  
   - Out-of-band scans for zero-day advisories (e.g., Log4j, Exchange ProxyShell).  
   - Scans for new system builds before production release.  

---

## 📌 Prioritization Model
- **Severity:** CVSS score + CISA Known Exploited Vulnerabilities (KEV) list.  
- **Impact:** Asset criticality and mission dependency.  
- **Exploitability:** Availability of proof-of-concept or in-the-wild exploit.  
- **Repeat Offenders:** Assets with recurring findings escalated to engineering leadership.  

---

## 📌 Remediation SLAs (Example)
| Severity  | SLA Timeline | Action |
|-----------|--------------|--------|
| Critical  | ≤ 15 days    | Immediate patch/config update |
| High      | ≤ 30 days    | Scheduled within next maintenance window |
| Medium    | ≤ 90 days    | Tracked and scheduled in quarterly cycle |
| Low       | ≤ 180 days   | Risk-accepted or addressed as resources allow |

Exceptions must be documented with compensating controls and ISSM approval.  

---

## 📌 POA&M Workflow
1. Export ACAS scan results to CSV/Excel.  
2. Normalize and import findings into a **POA&M tracker**.  
3. Assign remediation owner and due date.  
4. Track lifecycle status: **Open → Mitigated → Closed**.  
5. Review POA&M monthly with ISSM; archive closed items quarterly.  

### Example POA&M Table
| Vulnerability ID | System | Severity | Mitigation Action | Owner   | Due Date   | Status   |
|------------------|--------|----------|------------------|---------|------------|----------|
| V-12345          | DC-01  | Critical | Apply KB5028166  | WinOps  | 2025-07-15 | Closed   |
| V-67890          | DB-02  | High     | Apply STIG reg   | DBA     | 2025-08-01 | Open     |
| V-24680          | WEB-03 | Medium   | Patch OpenSSL    | WebOps  | 2025-09-10 | Mitigated |

---

## 📌 Metrics & Reporting
- **Critical vulns trend** (30/60/90 days).  
- **SLA compliance rate** by severity.  
- **Mean time to remediate (MTTR)** per vulnerability class.  
- **% assets scanned with valid credentials**.  
- **Repeat offender systems** (tracked for engineering escalation).  

Visualized in **Power BI or Excel dashboards**, exported monthly to leadership and quarterly to auditors.  

---

## ✅ Outcomes
- **25% reduction in critical vulns** in the first quarter of cadence adoption.  
- **100% SLA compliance** for audit-priority systems.  
- **Zero significant audit findings** during inspection.  
- **Improved coordination** between security, ops, and engineering teams.  

---

## 📂 Appendices
- **POA&M Template:** [`poam-tracking-template.csv`](./poam-tracking-template.csv)  
- **Dashboard KPI Examples** (redacted)  
- **Exception Register** (with review cycle dates)  

---
