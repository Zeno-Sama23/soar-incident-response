# Playbook: Brute Force Email Notification

## Trigger
Microsoft Sentinel Incident creation

## Linked Rule
Brute Force - Multiple Failed Signins (T1110.001)

## Action
Send email notification to SOC analyst via Outlook.com

## Flow
1. Sentinel detects 5+ failed sign-ins within 1 hour
2. Incident created in Sentinel
3. Logic App triggered automatically
4. Email alert sent to kamdemteddy23@gmail.com

## MITRE ATT&CK
- Tactic: Credential Access
- Technique: T1110.001 - Brute Force: Password Guessing

## Response Time
Automated — under 60 seconds from detection to notification
