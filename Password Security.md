## MFA Policy ##
## MFA Requirement ##
Policy:
Mandatory for all users (no exceptions)
Method:
Authenticator app on personal or company phone
Enrollment:
https://mfa.servicedesk-simulator.com/setup
Backup Codes:
5 codes issued at enrollment (save in secure location)
Identity Model:
On-prem Directory syncs to Cloud Identity via AD Connect - passwords are managed on-prem, MFA is managed in the cloud

## Enrollment Steps
1. Go to https://mfa.servicedesk-simulator.com/setup

2. Sign in with domain account (firstname.lastname@servicedesk-simulator.com)

3. Download Authenticator app (iOS or Android)

4. Follow in-app prompts to scan QR code OR enter setup key

5. Approve test notification from authenticator

6. Save backup codes in password manager (critical!)

7. Enrollment complete

## Verification Process
User receives prompt in Authenticator app

User taps Approve

Takes 5-10 seconds

Can use 6-digit code as backup if app unavailable

##n
Lost Phone Recovery
User cannot login without MFA

Helpdesk resets MFA enrollment from the Directory console (the change syncs to Cloud Identity)

User must re-enroll with new device

Issue new backup codes

Process:
30 minutes after identity verification