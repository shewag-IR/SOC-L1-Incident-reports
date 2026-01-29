# 🛡️ SOC L1 Incident Reports – Hands-On Blue Team Practice

This repository contains **realistic SOC Level-1 incident reports** derived from hands-on investigations conducted in a **production-style SOC lab environment**.

The objective of this project is to demonstrate **practical, job-ready SOC skills**—including alert triage, log correlation, incident validation, and structured reporting—rather than theoretical or simulated write-ups.

---

## 📌 What This Repository Demonstrates

- End-to-end **SOC L1 alert investigation workflows**
- Accurate **True Positive vs False Positive** decision-making
- Multi-source log analysis (web, system, IDS/IPS, endpoint)
- Evidence-driven incident documentation with clear timelines
- Incident classification and technique mapping using **MITRE ATT&CK**
- Clear escalation rationale aligned with real SOC operating procedures

Each report reflects how a SOC analyst would investigate, validate, and document security alerts in an operational environment.

---

## 📖 How to Read These Incident Reports

Each incident report in this repository follows a **structured SOC workflow** to mirror real-world blue team operations:

1. **Alert Source & Trigger**  
   Initial alert generated from SIEM / IDS / endpoint telemetry.

2. **Triage & Context Building**  
   Validation using supporting logs (web access logs, system logs, IDS alerts, endpoint activity).

3. **Investigation & Correlation**  
   Correlating attacker behavior across multiple data sources to confirm intent and impact.

4. **Verdict**  
   Classification as **True Positive / False Positive**, with justification.

5. **MITRE ATT&CK Mapping**  
   Relevant tactics and techniques mapped for adversary behavior understanding.

6. **Containment & Response**  
   Actions taken (blocking IPs, removing artifacts, containment steps).

7. **Escalation Decision**  
   Clear reasoning for escalation or closure based on impact and risk.

This structure ensures every report is **analyst-ready, reviewer-friendly, and SOC-aligned**.

---

## ⭐ Featured Incident

### 🔴 Web Shell Upload & Command Execution Detection

**Scenario:**  
A public-facing web server was compromised via malicious file upload, leading to **remote command execution and data exfiltration attempts**.

**Key Investigation Highlights:**
- Detected abnormal request spikes from a single IP
- Identified directory fuzzing and suspicious upload behavior
- Confirmed successful web shell upload
- Observed command execution via HTTP requests
- Correlated IDS alerts, web logs, and host-based audit logs
- Validated attacker commands executed on the system
- Contained the incident by removing the shell and blocking the attacker

**Final Verdict:**  
✅ **True Positive — Confirmed Web Shell Compromise**  
🚨 **Escalation Required due to command execution and data exfiltration risk**

This incident demonstrates **real-world attacker behavior**, not lab noise.

---

## 🎯 Focus of This Repository

- Build **SOC L1 investigation depth**
- Practice **real alert-to-incident workflows**
- Strengthen **evidence-based reporting**
- Develop confidence in **escalation decisions**
- Prepare for **entry-level SOC and Blue Team roles**

---

## 🔗 Connect With Me

- 💼 **LinkedIn:** https://linkedin.com/in/analystshewag  
- 🧠 **GitHub:** https://github.com/shewag-IR  

I’m actively building hands-on SOC experience and documenting real investigations as part of my blue team journey.

---

📌 *This repository is continuously updated as new incidents are investigated.*
