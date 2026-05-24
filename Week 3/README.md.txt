CYART SOC TEAM — WEEK 3
Advanced SOC Operations & Incident Response Simulation

This repository contains the Week 3 practical implementation of advanced SOC operations including:

Advanced Log Analysis
Threat Intelligence Integration
Incident Escalation Workflows
Alert Triage
Evidence Preservation
Full SOC Workflow Simulation

The project was performed in a Windows-based cybersecurity lab environment using modern SIEM, DFIR, and incident response tools.

Repository Structure
Week 3
│
├── Documentation
│   ├── day05_report.pdf
│   ├── incident_report.pdf
│   ├── soc_workflow_report.pdf
│
├── Notes
│   ├── threat_intelligence_notes.pdf
│   ├── advanced_log_analysis_notes.pdf
│   ├── incident_escalation_notes.pdf
│   ├── alert_triage_notes.pdf
│   ├── evidence_preservation_notes.pdf
│
├── Screenshots
│   ├── wazuh_alert.png
│   ├── metasploit_exploit.png
│   ├── elastic_dashboard.png
│   ├── crowdsec_block.png
│
├── Workflow
│   └── workflow_steps.md
│
└── README.md
Objectives

The objectives of this project were to:

Understand advanced SOC workflows
Perform SIEM-based log analysis
Integrate threat intelligence feeds
Investigate suspicious alerts
Practice incident escalation
Preserve forensic evidence
Simulate attack detection and response
Improve cybersecurity investigation skills
Lab Environment
Host System
Windows 11
PowerShell
Google Chrome
Oracle VirtualBox
Virtual Machines
Virtual Machine	Purpose
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
Project Workflow
1. Attack Simulation

A Samba vulnerability was exploited using Metasploit against a Metasploitable2 virtual machine.

Exploit Used
use exploit/multi/samba/usermap_script

The attack generated suspicious activity for SIEM monitoring.

2. Threat Detection

Wazuh detected:

Unauthorized shell activity
Suspicious PowerShell execution
Network anomalies
Exploitation attempts
3. Log Correlation

Elastic Security was used to correlate:

Windows Event Logs
DNS traffic
PowerShell activity
Authentication events
Network connections
4. Threat Intelligence Integration

Threat intelligence feeds from AlienVault OTX and VirusTotal were used to enrich alerts and validate Indicators of Compromise (IOCs).

5. Alert Triage

Suspicious PowerShell execution alerts were investigated and correlated with IOC intelligence and SIEM events.

6. Incident Escalation

High severity incidents were escalated to Tier 2 analysts using TheHive incident management workflows.

7. Evidence Preservation

Velociraptor and FTK Imager were used to collect:

Memory dumps
Network artifacts
Volatile evidence
SIEM logs

SHA256 hashing was used to maintain forensic integrity.

8. Threat Containment

Containment measures included:

VM isolation
IP blocking using CrowdSec
Restricting outbound communication
MITRE ATT&CK Techniques Used
Technique ID	Technique Name
T1078	Valid Accounts
T1210	Exploitation of Remote Services
T1059	Command and Scripting Interpreter
Key Learning Outcomes

This project provided practical experience in:

SOC operations
SIEM monitoring
Log analysis
Threat intelligence integration
Alert triage
Incident escalation
Digital forensics
Evidence preservation
Threat containment
Screenshots Included

The repository includes screenshots for:

Wazuh alerts
Metasploit exploitation
Elastic dashboards
CrowdSec blocking activity
TheHive escalation workflow
Conclusion

This project successfully demonstrated a complete end-to-end SOC workflow simulation using enterprise-grade cybersecurity tools within a Windows-based lab environment.

The implementation improved practical understanding of:

Cyber threat detection
Security monitoring
Threat investigation
Incident response
Digital forensics
SOC coordination
References
MITRE ATT&CK Framework
Wazuh Documentation
Elastic Security Documentation
Metasploit Unleashed
CrowdSec Documentation
AlienVault OTX
VirusTotal
Velociraptor Documentation
NIST SP 800-61 Incident Handling Guide
Author

Dishari Singha
