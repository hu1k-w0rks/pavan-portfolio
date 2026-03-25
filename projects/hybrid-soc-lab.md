# Microsoft Sentinel SIEM & SOAR Hybrid SOC Lab

## Overview
This project demonstrates a hybrid SOC lab built to simulate practical security monitoring, alert generation, triage, enrichment, and response workflows using Microsoft Sentinel and supporting Azure security components.

## Objective
To build a hands-on SOC environment that collects telemetry from both Windows and Linux systems, detects suspicious activity, supports analyst investigation, and automates part of the triage workflow.

## Technologies Used
- Microsoft Sentinel
- Azure Arc
- Azure Monitor Agent (AMA)
- Microsoft Entra ID
- Logic Apps
- VirusTotal
- Microsoft Defender Threat Intelligence
- Sophos Central / Sophos XDR
- Windows VM
- Ubuntu VM

## Environment Design
The lab was designed as a hybrid monitoring setup where telemetry from Windows and Ubuntu systems was onboarded into Microsoft Sentinel. Azure Arc and AMA were used for log ingestion and management. Endpoint visibility was supported with Sophos tooling, and cloud-related visibility was extended through Microsoft security integrations.

## Implemented Capabilities

### Centralized Telemetry
Configured telemetry collection from Windows and Ubuntu systems into Microsoft Sentinel to support detection and investigation across a mixed environment.

### RBAC with Microsoft Entra ID
Engineered a scalable RBAC model using Microsoft Entra ID groups to manage access to Microsoft Sentinel resources. This reduced manual administrative effort and helped enforce least-privilege access.

### Detection Engineering
Built KQL-based analytics rules to detect:
- Multiple failed logon attempts / brute-force behavior
- Suspicious PowerShell execution
- Linux privilege-escalation activity
- Ransomware-linked process-kill and defense evasion behavior

### SOAR Integration
Deployed and configured Logic App playbooks to automate incident enrichment and triage support. Integrated external intelligence sources including VirusTotal and Microsoft Defender Threat Intelligence to add investigation context to incidents.

## Investigation Workflow
1. Security telemetry ingested into Microsoft Sentinel
2. KQL analytics rule triggered on suspicious behavior
3. Incident generated inside Sentinel
4. Logic App playbook executed for enrichment
5. Threat intelligence context added to incident
6. Analyst reviewed findings and validated severity

## Outcome
This project improved my understanding of how SIEM, SOAR, endpoint visibility, and access control work together in a SOC environment. It also helped me think more practically about how to create useful alerts and reduce repetitive triage work.

## Screenshots to Add
- <img width="1864" height="944" alt="image" src="https://github.com/user-attachments/assets/d4f9082b-e442-4760-8c04-869639cb24c4" />

- Analytics rules page
- Incident details view
- Logic App playbook run
- Architecture diagram
