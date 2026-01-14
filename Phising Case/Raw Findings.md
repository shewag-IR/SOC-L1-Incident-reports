EventID :

86

Event Time :

Mar, 22, 2021, 09:23 PM

Rule :

SOC141 - Phishing URL Detected

Level :

Security Analyst

Source Address :

172.16.17.49

Source Hostname :

EmilyComp

Destination Address :

91.189.114.8

Destination Hostname :

mogagrocol.ru

Username :

ellie

Request URL :

http://mogagrocol.ru/wp-content/plugins/akismet/fv/index.php?email=ellie@letsdefend.io

User Agent :

Mozilla/5.0 (Windows NT 6.1; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.88 Safari/537.36

Device Action :

Allowed

The source ip belongs to Emily
The destianation ip is cleaned but the domain for requested url was flagged by more than 10 vendors as phishing & malware in virustotal. Abuseipdb also shows it was reported previously.

		Visit the web page using sandbox application. Below is the screenshot

![[Pasted image 20260114145530.png]]


- When was it accessed - Feb, 14, 2021, 12:13 PM
	- What is the source address - 172.16.17.49
- What is the destination address - 91.189.114.8
- Which user tried to access - EmilyComp
- What is User Agent - Mozilla/5.0 (Windows NT 6.1; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.88 Safari/537.36
- Is the request blocked- no
  
  
  Artifacts - 
  http://mogagrocol.ru/wp-content/plugins/akismet/fv/index.php?email=ellie@letsdefend.io
  91.189.114.8
  
	  http://162.241.242.173:8080/HQ9TemntfBzghL/3wz57awaSHlQrrnP/S78n2aUqY7U/
  162.241.242.173
  
  http://67.68.210.95/2SjAcA5VhhJiFjBQ/vvszin6AicmidnG5bg/DaDVVYvfEHlcIIcgcu/0U5UiIkaHankrHGa/FYSJmdQDj2ejni1UI/
  
  67.68.210.95
  
  Source Address :

172.16.17.49

Source Hostname :

EmilyComp
  
  
  Note - At Mar, 22, 2021, 09:23 PM SIEM detected a phishing URL from the  host EmilyComp.
  The requested url   
http://mogagrocol.ru/wp-content/plugins/akismet/fv/index.php?email=ellie@letsdefend.io
The firewall action for the request was allowed and the parameter email confirmed that the user submitted their email on the phishing site.
The url was flagged by 10+ vendors as phishing & malware in virustotal.
SIEM logs confirmed that
after accessing the phishign site immidiately two more url was requested from the same user which were classified as botnet in threat inteligence platforms.
Confirmed initial access via phishing.
Visited the url flagged by the SIEM, using sandbox tools, suspicious landing page.
Confirmed malicious activ 
