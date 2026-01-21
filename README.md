SOC Detection Lab — Blue Team Portfolio
Overview

This repository contains hands-on SOC detection engineering projects built using a self-hosted SIEM environment. The lab simulates real-world adversary behavior using Atomic Red Team and custom attack tooling, with detections created and validated using endpoint telemetry and security logs.

The goal of this project is to demonstrate practical SOC skills including alert creation, detection tuning, incident investigation, and MITRE ATT&CK mapping.

Lab Architecture

Core Components:

SIEM Platform: Wazuh

Endpoint Telemetry: Sysmon + Windows Security Logs

Attack Simulation: Atomic Red Team

Virtualization: VMware / VirtualBox

Analysis Tools: Wireshark, Autopsy, FTK Imager

Architecture Flow:

Attacker Simulation (Atomic Red Team)
        ↓
Compromised Windows Endpoint
(Sysmon + Event Logs)
        ↓
Wazuh Agent
        ↓
Wazuh Manager / SIEM
        ↓
Detection Rules → Alerts → Investigation

Detection Engineering Approach

Each detection project follows a standardized SOC workflow:

Simulate adversary technique

Capture endpoint and security telemetry

Identify behavioral indicators

Create detection logic

Validate alert generation

Tune false positives

Document results

All detections are mapped to the MITRE ATT&CK framework and tested using controlled attack execution.

Implemented Detection Use Cases
Credential Access

T1003 — Credential Dumping
Detection of LSASS access and suspicious memory dumping activity using Sysmon telemetry.

Execution [Planned]

T1059 — PowerShell Abuse
Detection of encoded command execution and suspicious PowerShell behavior.

Persistence [Planned]

T1136 — Local Account Creation
Monitoring unauthorized local account creation and privilege escalation attempts.

Lateral Movement [Planned]

T1550 — Pass-the-Hash Behavior
Detection of abnormal authentication patterns across multiple endpoints.

Command and Control [Planned]

T1071 — Beaconing Activity
Identification of suspicious outbound communication patterns and C2-style behavior.

Impact (Ransomware Indicators) [Planned]

T1490 — Shadow Copy Deletion [Planned]
Detection of volume shadow copy removal commonly associated with ransomware activity.

Repository Structure
SOC-Detection-Lab
│
├── credential_access
│   └── T1003_credential_dumping.md
│
├── execution
│   └── T1059_powershell_detection.md
│
├── persistence
│   └── T1136_local_account_creation.md
│
├── lateral_movement
│   └── T1550_pass_the_hash.md
│
├── command_and_control
│   └── T1071_beacon_detection.md
│
├── ransomware
│   └── T1490_shadow_copy_deletion.md
│
├── diagrams
│
├── screenshots
│
└── README.md

Documentation Format

Each detection file includes:

Attack technique description

MITRE ATT&CK ID

Log sources used

Detection logic explanation

Alert screenshots

False positive analysis

Tuning methodology

Investigation workflow

This mirrors real SOC detection documentation standards.

Skills Demonstrated

SIEM rule creation and alert tuning

Endpoint telemetry analysis (Sysmon)

SOC alert triage and investigation

MITRE ATT&CK mapping

Forensic artifact analysis

Malware behavior identification

Incident documentation

Certifications

Blue Team Level 1 (BTL1) — Gold Coin Distinction
Security Blue Team

Disclaimer

All attack simulations are performed in isolated lab environments for educational and defensive security purposes only. No production systems or unauthorized networks are involved.

Contact

LinkedIn: linkedin.com/in/mohammad-alquamah
GitHub: github.com/alquamah-blue

Tell me:

Do you want the Detection Documentation Template next?
