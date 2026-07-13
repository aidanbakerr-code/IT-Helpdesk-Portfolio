## Domain Credentials
Your domain account is the single login you use everywhere in this environment. There is no separate "admin" or "helpdesk" password to memorize.

## Your Credentials
Username:
your display name (the name shown on your profile)
Password:
Servicedesk2026!
This is the shared domain password every technician uses. Your user name is simply your own display name.

## Where You Use It
• Signing in to a domain-joined workstation (the lock screen / "Other user")
• Connecting through Remote Desktop - the Remote Login prompt
• Run as Administrator (UAC) in the remote Command Prompt - enter your domain credentials to elevate
• The first sign-in after a freshly deployed machine joins the domain
• Joining a machine to the domain during a manual setup
The One Exception
The Imaging Server deployment task sequence authenticates to the deployment share with its own deployment password (not a login you use interactively). See "Workstation Deployment & Domain Join" for that. Everything else uses your domain credentials.

## Notes
• Same user name + password whether you are onsite or remote.
• If a sign-in is rejected, confirm you typed your display name exactly and the password Servicedesk2026! with no trailing spaces.

## Run as Administrator (Elevated Access)
Some commands on a remote workstation need elevation (admin rights). You elevate with your own DOMAIN credentials - there is no separate local administrator account.

Credentials to Enter
Username:
your display name
Password:
Servicedesk2026!
These are your standard domain credentials (see the Domain Credentials article).

When to Elevate
• Running an elevated Command Prompt (Run as Administrator)
• Commands requiring admin: gpupdate /force, sfc /scannow, chkdsk, shutdown, net user, dism, sc, wmic
• Installing or repairing software on user workstations
• System diagnostics and advanced troubleshooting
How to Elevate
1. Open Command Prompt on the remote workstation

2. Click "Run as Administrator" in the terminal toolbar

3. Enter your domain credentials when prompted (UAC dialog)

4. The terminal title bar will show "Administrator:" when elevated

5. Admin-only commands will now execute successfully

Security Policy
• Only elevate during active remote support sessions
• All elevated command usage is logged in Event Viewer
• Report any suspected account compromise immediately to IT Security

## Service Accounts Reference
Service accounts are used by applications and automated processes. Do NOT use for interactive login.

svc-backup
Purpose:
Automated backup jobs on FILESERV01
Managed By:
Tier 3 - Infrastructure
Password:
Stored in credentials vault (Tier 3 access only)

svc-print
Purpose:
Print spooler service on PRINT01
Managed By:
Tier 2 - Server Team
Password:
Stored in credentials vault (Tier 2 access only)

helpdesk-install
Purpose:
Software installation on user workstations (domain admin service account)
Managed By:
IT Director
Password:
Stored in secure credentials vault (Tier 2 access only)
Usage:
Run installers with SYSTEM permissions - never share with users

Important
• Service account passwords are NOT the same as your domain credentials
• If a service account is locked out, escalate to the managing team
