# 🛡️ SOC L1 Incident Reports – Hands-On Blue Team Practice

This repository contains **realistic SOC Level-1 incident reports** created from hands-on investigations performed in a **production-style SOC lab**.

The goal of this project is to demonstrate **practical SOC skills**, including alert triage, log analysis, incident documentation, and framework-aligned reporting — not theoretical write-ups.

---

## 📌 What This Repository Demonstrates

- SOC Level-1 **alert investigation workflow**
    
- **True Positive / False Positive** decision making
    
- Evidence-based incident documentation
    
- Mapping incidents to **MITRE ATT&CK**
    
- Reporting aligned with **NIST Incident Response lifecycle**
    
- Clear, concise communication expected in a real SOC
    

All reports are written as if they were handled in an **enterprise SOC environment**.

---

## 🧪 Lab Environment Overview

The incidents in this repository were investigated using a custom-built SOC lab consisting of:

- **SIEM:** Splunk Enterprise
    
- **Endpoints:**
    
    - Windows (Security Logs, Sysmon)
        
    - Linux (auth.log, auditd, syslog)
        
- **Security Tooling:**
    
    - Wazuh (host-based detection & alerts)
        
    - Suricata (network intrusion detection)
        
- **Cloud Platform:** Google Cloud Platform (GCP)
    
- **Ticketing & Documentation:** Jira, Obsidian, GitHub
    

This setup allows simulation of **real-world attacks and detections**, not canned examples.

---

## 📂 Incident Reports Included

Each incident folder typically contains:

- Incident report (PDF / Markdown)
    
- Evidence screenshots (logs, alerts, dashboards)
    
- Detection logic references
    
- Severity classification
    
- MITRE ATT&CK mapping
    
- Analyst notes and closure rationale
    

### Examples of Investigated Incidents:

- Windows RDP brute-force attack
    
- Linux SSH brute-force attack
    
- Phishing email analysis
    
- Suspicious authentication activity
    
- Web application attack detection
    

---

## 📄 Incident Report Structure

All reports follow a consistent SOC-style structure:

1. Alert Summary
    
2. Incident Timeline
    
3. Evidence & Log Analysis
    
4. MITRE ATT&CK Mapping
    
5. Severity Assessment
    
6. Impact Analysis
    
7. Containment & Recommendations
    
8. Analyst Verdict & Closure
    

This mirrors how **L1 analysts are expected to document incidents in real SOCs**.

---

## 🎯 Purpose of This Repository

This project exists to:

- Build **job-ready SOC experience**
    
- Showcase hands-on blue team capability
    
- Serve as a **living portfolio** for SOC L1 roles
    
- Practice disciplined incident response documentation
    

This is **not** a learning notes repository — it is an **operational SOC artifact repository**.

---

## 👤 Author

**Shewag Bhattarai**  
SOC Analyst (L1) – Blue Team  
🔗 GitHub: [https://github.com/shewag-IR](https://github.com/shewag-IR)  
🔗 LinkedIn: [Shewag Bhattarai](https://www.linkedin.com/in/analystshewag/) 

---

## ⚠️ Disclaimer

All incidents are generated and analyzed in a **controlled lab environment** for educational and professional development purposes only.