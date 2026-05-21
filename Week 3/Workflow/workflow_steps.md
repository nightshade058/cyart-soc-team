Week 3 — Full SOC Workflow Steps
Repository

cyart-soc-team

Objective

The objective of this workflow was to simulate a complete SOC (Security Operations Center) incident lifecycle including:

Attack simulation
Threat detection
Log correlation
Threat intelligence integration
Alert triage
Incident escalation
Evidence preservation
Containment
Reporting

The project was performed in a Windows-based cybersecurity lab environment using multiple SOC and DFIR tools.

Lab Environment
Host Machine
Windows 11
PowerShell
Google Chrome
Oracle VirtualBox
Virtual Machines Used
Machine	Purpose
Kali Linux	Attacker Machine
Metasploitable2	Vulnerable Target
Windows VM	Monitoring & SIEM
Tools Used
Tool	Purpose
Metasploit	Attack Simulation
Wazuh	SIEM Monitoring
Elastic Security	Log Correlation
CrowdSec	Threat Blocking
TheHive	Incident Management
Velociraptor	Evidence Collection
FTK Imager	Memory Acquisition
VirusTotal	IOC Validation
AlienVault OTX	Threat Intelligence
Step 1 — Environment Setup
Activities Performed
Installed VirtualBox on Windows 11
Created virtual machines
Configured NAT/Internal networking
Installed monitoring tools
Verified connectivity between systems
Step 2 — Attack Simulation
Objective

Simulate exploitation of a vulnerable Samba service.

Metasploit Commands Used
msfconsole
use exploit/multi/samba/usermap_script
set RHOST 192.168.1.101
exploit
Result
Reverse shell obtained
Unauthorized access established
Suspicious activity generated for SOC monitoring
Step 3 — Detection Using Wazuh
Activities

Wazuh detected:

Unauthorized shell activity
Suspicious PowerShell execution
Network anomalies
Exploitation attempts
Detection Example
Timestamp	Alert Description	Severity
2025-08-18 14:00:00	Samba Exploit Detected	High
Step 4 — Log Correlation in Elastic Security
Activities

Elastic Security was used to correlate:

Authentication logs
DNS traffic
PowerShell events
Network connections
Correlated Events
Event ID	Description
4625	Failed Login
4688	Process Creation
T1059	PowerShell Activity
Step 5 — Threat Intelligence Integration
Activities

Threat intelligence feeds from AlienVault OTX were integrated into Wazuh.

IOC Validation

Indicators were validated using:

VirusTotal
AlienVault OTX
Example IOC
IOC Type	Value	Reputation
IP Address	192.168.1.101	Malicious
Step 6 — Alert Triage
Activities

The suspicious PowerShell alert was investigated.

Investigation Included
IOC analysis
Threat intelligence validation
Log correlation
PowerShell review
Step 7 — Incident Escalation
Activities

A High-priority incident was created in TheHive.

Escalation Reasons
Confirmed exploitation
Shell access obtained
Suspicious outbound traffic
Threat intelligence IOC match
Step 8 — Evidence Preservation
Volatile Data Collection

Velociraptor was used to collect:

Network connections
Running processes
Memory artifacts
Commands Used
SELECT * FROM netstat
Artifact.Windows.Memory.Acquisition
Evidence Hashing

SHA256 hashing was used to maintain evidence integrity.

Step 9 — Containment
Actions Taken
Isolated compromised VM
Blocked attacker IP using CrowdSec
Disabled suspicious sessions
Restricted outbound traffic
Step 10 — Reporting
Reports Created

The following reports were prepared:

day05_report
incident_report
soc_workflow_report
threat_intelligence_notes
advanced_log_analysis_notes
incident_escalation_notes
alert_triage_notes
evidence_preservation_notes
MITRE ATT&CK Techniques Used
Technique ID	Technique Name
T1078	Valid Accounts
T1210	Exploitation of Remote Services
T1059	Command and Scripting Interpreter
Key Learning Outcomes

This project provided practical experience in:

SIEM monitoring
Threat detection
Log analysis
Threat intelligence integration
SOC workflows
Incident escalation
Evidence preservation
Threat containment
SOC reporting
Conclusion

The SOC workflow simulation successfully demonstrated an end-to-end cybersecurity incident lifecycle using enterprise-grade security monitoring and incident response tools within a Windows-based lab environment.

The project improved practical understanding of real-world SOC operations, threat investigation workflows, and incident response coordination.