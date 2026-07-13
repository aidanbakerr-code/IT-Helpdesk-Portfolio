## Approved Software List ##
## All Users (No Request Required):
• Office Suite (documents, Chat, Cloud Drive)
• Video Meet (video conferencing, auto-licensed)
• Team Messenger (instant messaging, auto-licensed)
• Google Chrome (browser, pre-installed)
• Mozilla Firefox (browser, pre-installed)

Request Required (Department-Specific):

• PDF Reader Pro (readers, writers, designers) - Limited 25 seats
• Code Editor (Engineering only) - Unlimited
• CAD Studio (Engineering only) - Limited 10 seats
• Accounting Suite Desktop (Finance/Accounting only) - Limited 15 seats
• CRM Platform (Sales only) - Limited per sales rep
• Issue Tracker (Engineering only) - Limited per engineer

## Request Process
1. User requests from manager > Manager approves
2. Manager submits ticket to IT helpdesk with:
• Employee name, department
• Software requested
• Business justification
• Estimated duration (1 year typical)
3. IT checks approved list + license availability
4. If approved: Install via Imaging Server or manual, assign license
5. If denied: Explain reason (not approved, no licenses, not for your dept)

## Prohibited Software
• Peer-to-peer file sharing (BitTorrent, etc.)
• Unlicensed/cracked software
• Personal social media apps (on company machines)
• Games (except approved work-related tools)
• VPN clients other than the company VPN client
• Antivirus other than the built-in antivirus (IT-managed)

## Current License Status
Office Suite E3
• Total Seats: 500
• In Use: 472 seats
• Available: 28 seats
• Cost per Seat: $12/month
• Renewal: Auto-renew monthly

Design Suite
• Total Seats: 25
• In Use: 23 seats
• Available: 2 seats
• Request Time: Tier 1 escalates to Tier 2
• Cost per Seat: $55/month

Video Meet Pro
• Total Seats: 200
• In Use: 185 seats
• Available: 15 seats
• Cost per Seat: $200/year per user
• Renewal: December 2026

CAD Studio
• Total Seats: 10
• In Use: 8 seats
• Available: 2 seats
• Engineering-only, contact engineering manager
• Cost per Seat: $520/year

Accounting Suite Desktop
• Total Seats: 15
• In Use: 12 seats
• Available: 3 seats
• Finance/Accounting-only
• Cost per Seat: $400/year

CRM Platform
• Total Seats: Dynamic (per sales team size)
• Current Users: Based on sales rep roster
• Renewal: Quarterly review with sales manager

Issue Tracker
• Total Seats: 25 (development team)
• In Use: 18 seats
• Available: 7 seats
• Engineering allocation, Tier 2 manages


## Imaging Server Self-Service Portal (Recommended)
URL:
selfservice.servicedesk-simulator.com
Authentication:
Domain credentials (auto-login on domain machine)
Availability:
Most approved software (Office Suite, Video Meet, Team Messenger, etc.)
Installation Time:
10-15 minutes (background install)
Advantages:
User controls timing, no IT remote access needed, automatic license assignment
Steps:
1. Go to selfservice.servicedesk-simulator.com
2. Click "Available Software"
3. Browse or search for application
4. Click "Install" or "Request"
5. Application downloads and installs automatically
6. Restart prompt appears when ready
7. Complete, icon appears on Start menu

## Manual Installation (Non-Imaging Server Apps)
When Used:Specialized software not in Imaging Server (Design Suite, CAD Studio, Accounting Suite)
Authentication:Helpdesk must remote in with elevated (admin) account
Steps:
1. IT opens ticket, schedules install time
2. IT remotes into user workstation
3. IT downloads installer from official publisher site
4. IT runs installer with admin rights (helpdesk-install account)
5. IT follows wizard, declines unnecessary toolbars/extras
6. IT tests application launch
7. IT closes remote session
8. User confirms install, IT documents in ticket

## Admin Credentials Required
Account:
helpdesk-install (domain admin service account)
Purpose:
Run installers with SYSTEM permissions
Password:
Stored in secure credentials vault (Tier 2 access only)
Never:
Share with users, give credentials to users, allow user-run installations
Logging:
All installs logged in Event Viewer for compliance