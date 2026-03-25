# Endpoint Threat Detection & Investigation using Sophos XDR

## Overview
This project focuses on endpoint-level threat detection and investigation using Sophos XDR. Multiple attack scenarios were simulated on Windows and Ubuntu systems to analyze detection behavior, investigate alerts, and understand attack patterns using real-world SOC workflows.

## Objective
To gain hands-on experience in endpoint detection and response (EDR/XDR), including threat identification, process analysis, MITRE ATT&CK mapping, and investigation using threat graphs.

## Technologies Used
- Sophos Central
- Sophos XDR
- Windows VM
- Ubuntu VM

## Attack Simulations & Investigations

### 1. Ransomware Detection (WannaCry Simulation)

Simulated ransomware-like behavior using a WannaCry sample to validate endpoint detection and investigation capabilities.

**Detection Details**
- Source: Sophos XDR
- Severity: Critical
- Detection Name: WIN-PROT-VDL-MALWARE-TROJ-RANSOM-EMG

**Key Observations**
- Malicious process linked to `explorer.exe`
- File and registry activity consistent with ransomware behavior
- External communication with suspicious domains (beaconing)

**MITRE ATT&CK Mapping**
- Impact (T1486 – Data Encrypted for Impact)
- Defense Evasion
- Execution

**Investigation**
- Analyzed Sophos Threat Graph to trace attack flow
- Identified root cause process (`explorer.exe`)
- Reviewed file operations, registry modifications, and network connections
- Correlated impacted device, user, and IP indicators

**Screenshots**
<img width="1594" height="864" alt="Screenshot_2026-03-25_14-28-11" src="https://github.com/user-attachments/assets/5bd641e7-648f-4837-b804-80cb8a0e5878" />
<img width="1591" height="768" alt="Screenshot_2026-03-25_14-28-31" src="https://github.com/user-attachments/assets/62874404-9128-458d-b469-cb2152769c62" />
---

### 2. EICAR Malware Detection

Executed the EICAR test file to validate real-time malware detection capabilities.

**Detection Details**
- Source: Sophos XDR
- Severity: Medium
- Detection Type: Test Malware

**Key Observations**
- Immediate detection upon execution
- File identified as known test malware
- No significant system impact due to controlled environment

**Investigation**
- Reviewed detection details and classification
- Validated alert generation within Sophos Central
- Confirmed endpoint protection response

**Screenshots**
<img width="1580" height="860" alt="Screenshot_2026-03-25_14-26-26" src="https://github.com/user-attachments/assets/c661689b-9691-421c-a602-1157785fe53b" />

---

### 3. Ubuntu Brute Force & Python PTY Spawn Detection

Simulated suspicious activity on an Ubuntu system including brute-force-like behavior and interactive shell spawning.

**Detection Details**
- Source: Sophos XDR / Sophos Central
- Severity: Medium
- Detection Name: UNX-EXE-PRC-PYTHON-PTY-SPAWN-SHELL-1

**Observed Activity**
- Suspicious command execution:
  `python3 -c import pty; pty.spawn("/bin/bash")`
- Behavior associated with unauthorized shell access and credential-related activity

**MITRE ATT&CK Mapping**
- Execution (T1059)
- Credential Access

**Investigation**
- Analyzed command-line activity and process (`python3`)
- Reviewed impacted entities:
  - Device (Ubuntu VM)
  - User (wtmp)
  - IP addresses
- Validated detection against simulated attack scenario

**Screenshots**
(Add your Ubuntu detection screenshots here)

---

## Investigation Workflow

1. Suspicious activity executed on endpoint (Windows / Ubuntu)
2. Detection triggered in Sophos XDR
3. Alert generated in Sophos Central
4. Analyst reviewed:
   - Detection details
   - Command-line activity
   - Impacted entities (device, user, IP)
5. Threat Graph used to:
   - Identify root cause
   - Trace process relationships
   - Analyze file, registry, and network activity
6. MITRE ATT&CK techniques identified
7. Incident validated and documented

---

## Key Skills Demonstrated

- Endpoint Detection & Response (EDR/XDR)
- Threat investigation using process trees and threat graphs
- MITRE ATT&CK mapping
- Malware behavior analysis (ransomware simulation)
- Linux and Windows security monitoring
- Command-line and process-level analysis
- Incident triage and validation

---

## Outcome

This project improved my ability to analyze endpoint-level threats, understand attacker behavior, and perform structured investigations using XDR tools. It also helped me gain practical experience in correlating alerts with real attack simulations and applying MITRE ATT&CK methodology in investigations.
