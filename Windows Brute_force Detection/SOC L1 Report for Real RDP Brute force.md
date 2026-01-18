**INCIDENT RESPONSE REPORT** **Incident ID:** INC-2026-001 **Date:** January 18, 2026 **Analyst:** Shewag Bhattarai **Severity** : Medium  **Status:**   Closed / Resolved.

![[Pasted image 20260118193400.png]]
![[Pasted image 20260118195026.png]]

**1. Executive Summary** On January 18, 2026, the SOC detected a high-volume RDP Brute Force attack targeting the external-facing Windows (`Part of my soc-server`). The detection logic triggered after identifying 4,884 failed login attempts within a short timeframe. Investigation confirmed the activity originated from a known malicious IP address in Ukraine. No successful authentication events were observed; the attack was unsuccessful.

![[Pasted image 20260118193441.png]]

**2. Incident Details**

- **Attack Vector:** Remote Desktop Protocol (Port 3389)
    
- **Detection Source:** Splunk Enterprise (WinEventLog:Security)
    
- **Event Code:** 4625 (Logon Failure)
    
- **Total Attempts:** 4,884
    
- **Timeframe:** 17:24 IST - 19:24 IST (approx)
    

**3. Threat Intelligence**

![[Pasted image 20260118193505.png]]

- **Attacker IP:** `185.243.96.63`
    
- **ASN/ISP:** Rices Privately Owned Enterprise
    
- **Reputation:** Malicious. Flagged by 1/93 vendors on VirusTotal (Forcepoint ThreatSeeker) as a known scanner.
    

**4. Investigation & Analysis**

![[Pasted image 20260118193547.png]]
- **Triage:** Queried Splunk for `EventCode=4624` (Successful Logon) associated with the source IP `185.243.96.63`.
    
- **Result:** Zero results returned.
    
- **Conclusion:** The attacker attempted a dictionary attack but failed to guess valid credentials.
    

**5. Containment & Recommendations**

- **Immediate Action:** IP address verified as external threat.
    
- **Recommendation:** Adding `185.243.96.63` to the network firewall blocklist (Deny Inbound).
    
- **Long-term Recommendation:** Disabled RDP exposure to the open internet and enforce VPN-only access for administration