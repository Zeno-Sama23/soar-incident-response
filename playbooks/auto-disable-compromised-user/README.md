# Playbook: Auto Disable Compromised User

## Trigger
Microsoft Sentinel Incident creation

## Linked Rule
Brute Force - Multiple Failed Signins (T1110.001)

## Action
Automatically disables the compromised user account in Microsoft Entra ID

## Flow
1. Sentinel detects 5+ failed sign-ins within 1 hour
2. Incident created in Sentinel
3. Logic App triggered automatically
4. User account disabled via Microsoft Entra ID connector
5. Attacker loses access immediately

## MITRE ATT&CK
- Tactic: Credential Access
- Technique: T1110.001 - Brute Force: Password Guessing

## Response Time
Automated — under 60 seconds from detection to account lockdown
