# Ransomware Detection & Investigation Case Study (WannaCry Simulation)

## Scenario
A ransomware sample (WannaCry) was executed in a controlled lab environment to observe endpoint detection behavior and perform a structured investigation using Sophos XDR.

## Objective
To analyze ransomware activity from a SOC analyst perspective by:
- Validating detection mechanisms
- Investigating process behavior and attack flow
- Mapping activity to MITRE ATT&CK techniques
- Verifying endpoint response effectiveness

---

## Environment
- Windows VM (target system)
- Sophos Endpoint / Sophos XDR
- Isolated lab setup

---

## Detection Details

- **Detection Source:** Sophos XDR  
- **Severity:** Critical  
- **Detection Name:** WIN-PROT-VDL-MALWARE-TROJ-RANSOM-EMG  
- **Initial Process:** `explorer.exe`  
- **Associated Indicator:** `wannacry.exe`

The ransomware was detected during execution based on behavioral indicators.

---

## Investigation Process

### 1. Initial Alert Review
- Reviewed alert details in Sophos Central
- Identified affected endpoint and user context
- Confirmed severity as **Critical**

---

### 2. Threat Graph Analysis
Used Sophos Threat Graph to visualize attack flow:

- Root cause process: `explorer.exe`
- Malicious payload: `wannacry.exe`
- Observed relationships between processes and system activity

---

### 3. Behavioral Analysis

The following suspicious behaviors were observed:

- File access and modification activity
- Registry key interactions
- Process execution patterns consistent with ransomware
- Network communication (beaconing behavior)

---

### 4. MITRE ATT&CK Mapping

The activity aligned with the following techniques:

- **Impact (T1486 – Data Encrypted for Impact)**
- **Execution**
- **Defense Evasion**

---

### 5. Impact Assessment

- No real data impact due to controlled lab environment
- Malicious activity was detected early
- Endpoint protection prevented further propagation

---

## Response & Containment

- Threat was automatically blocked by Sophos Endpoint
- No lateral movement observed
- No additional remediation required due to successful containment

---

## Key Findings

- Detection was triggered using behavioral analysis rather than signature alone
- Threat Graph provided clear visibility into attack chain and root cause
- Endpoint telemetry enabled detailed investigation of process, file, and network activity
- Early detection significantly reduced potential impact

---

## Lessons Learned

- Behavioral detection is essential for identifying ransomware activity
- Process-level visibility is critical for root cause analysis
- Threat graphs simplify complex attack investigation
- Endpoint detection tools play a key role in rapid containment

---

## Screenshots
<img width="1614" height="504" alt="image" src="https://github.com/user-attachments/assets/ad057304-7476-4d5f-8548-308275c58b09" />

<img width="1589" height="714" alt="image" src="https://github.com/user-attachments/assets/d0e2c4e3-2528-4bf1-95f6-92879a6de166" />

<img width="1549" height="240" alt="image" src="https://github.com/user-attachments/assets/5464a234-1396-45ed-a396-9d9c29ae1bcf" />

<img width="1594" height="864" alt="Screenshot_2026-03-25_14-28-11" src="https://github.com/user-attachments/assets/7f1d2dc0-edf6-49b8-a1be-224e8f99905c" />

<img width="1591" height="768" alt="Screenshot_2026-03-25_14-28-31" src="https://github.com/user-attachments/assets/3569dee1-a16d-4660-9cb4-262954d71789" />

<img width="1607" height="889" alt="Screenshot_2026-03-25_14-47-36" src="https://github.com/user-attachments/assets/f7071b5a-088c-4fb4-b05b-7de1a22aace3" />
