# Detection Engineering Notes (KQL – Microsoft Sentinel)

## Focus
This document outlines my practical approach to building KQL-based detections in Microsoft Sentinel, with emphasis on real attacker behavior, investigation context, and SOC usability.

---

## Detection Areas Covered

- Brute-force login attempts
- Suspicious PowerShell execution
- Linux privilege escalation activity
- Ransomware defense evasion behavior
- Process-kill activity associated with ransomware

---

## Detection Design Approach

When building detections, I focus on:

### 1. Behavior-Based Detection
Prioritize attacker behavior over static indicators.  
Example: identifying suspicious process execution patterns rather than relying only on known malware signatures.

### 2. Investigation Context
Ensure alerts provide useful context for analysts:
- Process name
- Command line
- User account
- Host/device
- Timestamp

### 3. Noise Reduction
Avoid high-volume, low-value alerts by:
- Filtering common benign activity
- Narrowing detection conditions
- Focusing on suspicious combinations of events

### 4. SOC Usability
Design detections that:
- Are easy to understand
- Support quick triage
- Help analysts move from alert → investigation quickly

---

## Example Detection: Ransomware Process-Kill Behavior

Ransomware often attempts to disable security tools, terminate backup services, or kill critical processes before encryption.

### Detection Logic Focus
- Identify suspicious use of process termination commands
- Monitor abnormal usage of tools capable of killing processes
- Correlate with other suspicious activity where possible

### Investigation Value
This type of detection helps identify:
- Early-stage ransomware behavior
- Defense evasion attempts
- Potential pre-encryption activity

---

## Example Detection: Brute Force Login Attempts

### Detection Logic Focus
- Multiple failed login attempts within a short time window
- Repeated authentication failures from the same IP or user

### Investigation Value
- Helps identify credential attack attempts
- Supports early detection of unauthorized access attempts

---

## Example Detection: Suspicious PowerShell Execution

### Detection Logic Focus
- Encoded commands
- Unusual execution patterns
- PowerShell spawned from suspicious parent processes

### Investigation Value
- Detects potential post-exploitation activity
- Identifies attacker-controlled execution

---

## Key Skills Demonstrated

- KQL-based detection design in Microsoft Sentinel
- Understanding of attacker behavior patterns
- Alert tuning and noise reduction
- Building investigation-friendly alerts
- Mapping detections to MITRE ATT&CK techniques

---

## Outcome

This work helped me understand how to design detections that are not just technically correct, but also practical and useful in a SOC environment. The focus was on improving detection quality, reducing alert fatigue, and supporting efficient analyst workflows.
