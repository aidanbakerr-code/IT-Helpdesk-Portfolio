
## Support Tiers & SLAs 
## Tier 1 (Help Desk - YOU)

• Responsibility: First point of contact for all tickets
• Response Time: 15 minutes (acknowledge ticket exists)
• Resolution Target: 4 hours for standard issues
• Scope: Password resets, printer setup, basic troubleshooting, account unlocks
• When to Escalate: Can't resolve in 30 min, technical issue beyond knowledge, server down
• Escalate To: Create ticket assign to Tier 2, include diagnostics

## Tier 2 (System Administrators)

• Responsibility: Complex technical issues, system troubleshooting
• Response Time: 1 hour
• Resolution Target: 8 hours
• Scope: Network issues, server problems, software deployment, domain controller issues, device policy
• When to Escalate: Server outage, replication failure, security incident, vendor needed
• Escalate To: Create High priority ticket, page on-call admin via Chat

## Tier 3 (Engineering / Vendors)

• Responsibility: Specialized hardware/software vendors, critical infrastructure
• Response Time: 4 hours
• Resolution Target: 24 hours
• Scope: Vendor hardware support, appliance configuration, specialized app troubleshooting
• When Used: Hardware RMA, Vendor Premier Support, ISP issues
• Contact: Use vendor support numbers (see Vendor Support section)

## Critical/Outage (Immediate Escalation)

• Definition: Server down, security breach, loss of email/network, multiple users affected
• Response: Immediate (all hands on deck, page everyone)
• Escalate To: Manager + on-call admin (via Chat #it-oncall channel)
• Example Issues: EXCH01 offline, Mail Server database corruption, firewall failure, malware detected


## Vendor Support Contacts ##
## Tier 1 IT Helpdesk (Internal)
Phone:
Ext. 5555 (main number)
Email:
helpdesk@servicedesk-simulator.com
Hours:
8 AM - 6 PM Monday-Friday (EST)
Chat:
Chat channel #it-helpdesk (available during business hours)
Portal:
helpdesk.servicedesk-simulator.com (ticket system)

## Hardware Support (Premium Support)
Phone:
1-800-456-3355
Hours:
24/7/365 (premium support)
Required Info:
Service Tag (bottom of computer), Contract #
Typical:
Next business day onsite for hardware replacement
Setup:
Contract SDSim-HW-2024 (Tier 2 has account info)
Scope:
Desktop repairs, laptop repairs, docking station issues

## Vendor Premier Support
Phone:
1-800-936-5800
Hours:
24/7/365
Account:
SDSim-MS-2024 (contract ID in Tier 2 system)
Services:
Server OS, Mail Server, Office Suite, Cloud Platform
Escalation:
Use for critical bugs, security patches, Mail Server issues
Response:
1 hour (Premier tier SLA)

## Metro ISP (Internet Service Provider)
Phone:
1-888-812-2591
Hours:
24/7 for outages, 7 AM - 7 PM for non-emergency
Account:
8834-2291-01 (main account number)
Line:
Fiber 1Gbps symmetrical, uptime SLA 99.9%
Contact:
For internet down, BGP route issues, packet loss
Typical:
ISP tech will test connection from network edge

## Printer Vendor Support
Phone:
1-800-474-6836
Hours:
8 AM - 10 PM EST Monday-Saturday
Scope:
Printer hardware issues (not PRINT01 server)
Info Needed:
Model (e.g. Printeck PT-4200), Serial # (under printer)
Typical:
Troubleshooting, cartridge replacement, hardware swap
Alternative:
Check the printer vendor's site for drivers/support for remote troubleshooting

## Weekly On-Call Schedule
Rotation:
Changes every Monday at 9 AM
On-Call Person: Pinned in Chat #it-oncall channel

Schedule Source:
IT Manager posts in #it-oncall at week start
Contact:
Phone number posted in channel (personal mobile)

##On-Call Responsibilities
During Business Hours (8 AM - 6 PM): Part of Tier 2 team, handle normal escalations

After Hours (6 PM - 8 AM): EMERGENCY ONLY response (not routine tickets)

Weekends:
EMERGENCY ONLY (leave normal tickets for Monday)
On Call Availability:
Personal phone, expected to answer within 15 minutes

## What Constitutes Emergency (On-Call)
Yes, Call On-Call:

• Email server (EXCH01) completely down (no one can send/receive mail)
• File server (FILESERV01) inaccessible (no one can access files)
• Network completely down (no internet, no WiFi, core router issue)
• Security breach suspected (malware, unauthorized access, data leak)
• Domain Controller failure (AD replication down, users cannot login)
• Multiple building (all floors) without network (campus-wide outage)
No, Don't Call On-Call:

• Single user printer issue (wait until morning)
• One person's monitor flickering (wait until morning)
• Software installer not available (wait until morning)
• Password reset request (user can wait 8 hours)
• General question about setup (wait until morning)

## Escalation Process
1. Tier 1 (You) Attempts resolution for 30 minutes

2. Still unresolved? Page on-call via Chat: @on-call [brief issue description]

3. On-call person responds, takes over ticket

4. On-call person remote into systems, diagnoses, implements fix

5. Follow up: Document in ticket next business day
