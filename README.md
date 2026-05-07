# Automated Incident Response with SOAR

## Overview
Three Logic Apps playbooks integrated with Microsoft Sentinel for automated incident response, reducing Mean Time To Respond (MTTR).

## Stack
- Microsoft Sentinel
- Azure Logic Apps
- Microsoft Entra ID
- VirusTotal API v3
- Outlook.com (notifications)

## Playbooks

| Playbook | Trigger | Action | MITRE ATT&CK |
|----------|---------|--------|-------------|
| Brute Force Email Notification | Incident created | Email alert via Outlook | T1110.001 |
| Auto Disable Compromised User | Incident created | Disable Entra ID account | T1110.001 |
| IP Enrichment via VirusTotal | Incident created | Add VT report to incident | T1078.004 |

## Key Metrics
- **MTTR:** Reduced from manual (hours) to automated (< 60 seconds)
- **Coverage:** 3 automated responses across 2 detection rules
- **Integration:** Sentinel → Logic Apps → Entra ID / VirusTotal

## Skills Demonstrated
- SOAR playbook design and implementation
- API integration (VirusTotal v3)
- Automated user account management
- Incident enrichment with threat intelligence
- End-to-end IR automation
