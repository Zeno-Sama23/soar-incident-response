# Playbook: IP Enrichment via VirusTotal

## Trigger
Microsoft Sentinel Incident creation

## Linked Rule
Suspicious Privileged Role Assignment (T1078.004)

## Action
Automatically enriches Sentinel incidents with VirusTotal IP reputation data

## Flow
1. Sentinel creates an incident
2. Logic App triggered automatically
3. HTTP GET request to VirusTotal API v3
4. IP reputation data retrieved (malicious score, country, ASN)
5. Results added as comment directly in the Sentinel incident

## MITRE ATT&CK
- Tactic: Privilege Escalation
- Technique: T1078.004 - Valid Accounts: Cloud Accounts

## Value
- Reduces analyst investigation time
- Automatic threat intelligence enrichment
- No manual VirusTotal lookups needed
