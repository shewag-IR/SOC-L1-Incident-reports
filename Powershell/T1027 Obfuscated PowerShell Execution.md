
## 🛡️ SOC Lab: PowerShell Obfuscation Detection & Triage (T1027)

## 📝 Executive Summary

On February 13, 2026, I investigated a high-severity alert involving obfuscated PowerShell execution on a Windows endpoint. By leveraging a direct **Splunk-to-SOAR** pipeline, I identified, triaged, and resolved a True Positive reconnaissance attempt. The investigation confirmed an attacker (emulated via Atomic Red Team) utilized Base64 encoding to mask administrative group discovery commands.

## 🛠️ The Tech Stack

- **SIEM:** Splunk Enterprise (Direct Ingestion via Universal Forwarder).
    
- **SOAR:** Splunk SOAR (Orchestration & Triage).
    
- **Endpoint Telemetry:** Sysmon & Windows Event Logs.
    
- **Analysis Tools:** CyberChef.
    

## 🛡️ The Detection Pipeline

1. **Telemetry:** Sysmon Event ID 1 (Process Creation) captured the execution on the host.
    
2. **Ingestion:** Logs were indexed in Splunk, where a custom hunting query identified the `-EncodedCommand` flag.
    
3. **Orchestration:** Splunk automatically triggered an event in SOAR, passing structured CEF artifacts including the Base64 payload and the victim's username.
    

## 🔍 Technical Analysis & Findings

The suspicious command captured by the SIEM was:

`powershell.exe -ExecutionPolicy Bypass -WindowStyle Hidden -EncodedCommand bgBIAHQAIABSAG8AYWBHAGWAZ BYAG8AdQBWACAAYQBKAGBAAQBUAGKACWBBAHIAYQBOAGBACgBZAA==`

**Analysis Steps:**

- **Extraction:** Isolated the `Encoded string` artifact within the Splunk SOAR investigation container.
    
- **De-obfuscation:** Utilized CyberChef with a `From Base64` and `Decode text (UTF-16LE)` recipe to effectively strip null bytes inherent to Windows PowerShell encoding.
    
- **Result:** The decoded command was revealed to be `net localgroup administrators`, confirming a reconnaissance attempt to identify administrative privileges.
    

## 🗺️ MITRE ATT&CK Mapping

## 🏁 Resolution & Timeline

The incident was classified as a **True Positive**.

- **15:40:** Alert triggered in Splunk and ingested into SOAR.
    
- **15:44:** Ticket assigned to analyst and status moved to `Open`.
    
- **15:52:** Payload decoded; confirmed malicious intent.
    
- **15:56:** Incident successfully closed as a True Positive.
    

**Mean Time to Resolve (MTTR):** 16 minutes.