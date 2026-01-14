On Mar 22, 2021 at 09:23 PM, SIEM detected access to a known phishing URL 
(http://mogagroco.ru/wp-content/plugins/akismet/fv/index.php?email=elletsdefend)
originating from host EmilyComp. The request was allowed by the firewall.

Investigation confirmed that the user submitted their email address on the phishing
page, indicating successful interaction. URL reputation analysis via VirusTotal 
identified the domain as malicious, flagged by more than 10 security vendors.

Following the initial access, multiple additional URLs were requested from the same
host. Threat intelligence platforms classified this follow-on activity as botnet-
related behavior. Sandbox analysis confirmed the presence of a credential harvesting
landing page.

No evidence of lateral movement or further compromise was observed beyond the 
affected host.

Conclusion: This activity was confirmed as a successful phishing attack with user
interaction.

Remediation Actions:
- User credentials reset
- User notified and security awareness guidance provided
- Malicious URLs blocked at proxy level
- Host monitored for additional suspicious activity

Verdict: True Positive
