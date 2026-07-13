## Domain Controllers
## DC01 (Primary Domain Controller)
IP Address:
10.0.2.10
Location:
Server Room A
Role:
Primary Domain Controller (holds all FSMO roles)
OS:
Server OS 2022 Standard
AD Replication:
Every 15 minutes with DC02
DNS:
Primary DNS for servicedesk-simulator.com
DHCP:
Primary DHCP server for all subnets
Services:
AD, DNS, DHCP, NTP time server

## DC02 (Secondary Domain Controller)
IP Address:
10.0.2.11
Location:
Server Room B
Role:
Secondary Domain Controller (replication partner)
OS:
Server OS 2022 Standard
AD Replication:
Every 15 minutes (pulls from DC01)
DNS:
Secondary DNS for fallback
Services:
AD, DNS, backup DHCP
Failover:
Can take FSMO roles if DC01 unavailable

## FSMO Roles (Held by DC01)
PDC Emulator:
Password replication, time source
RID Master:
Account creation authorization
Infrastructure Master:
Cross-domain references
Schema Master:
AD schema changes
Domain Naming Master:
Forest-wide operations


## Troubleshooting
Replication Error:
Check network between datacenters, run repadmin /syncall, restart NTDS service
Slow Login:
Check DC01 CPU/memory, verify DNS working, run DCDIAG
Cannot Create Users:
Check RID pool not exhausted (DC01 issue), contact Tier 2

## Mail Server ##
##EXCH01 Specifications
IP Address:
10.0.2.20
Location:
Server Room A
OS:
Server OS 2022 Standard
Mail Server Version:
Mail Server 2019 CU14
Database Size:
2TB total capacity
Max Mailbox Size:
5GB per user (enforced)

## Services & Access
Webmail Access:
https://mail.servicedesk-simulator.com/owa
IMAP:
Disabled (for security policy)
SMTP Relay:
10.0.2.20 port 587 (requires auth)
ActiveSync:
Enabled (for mobile devices)
Autodiscover:
Configured for Mail auto-configuration

## Database Details
Mailbox Database:
MailDB
Location:
E:\MailDB (500GB SSD RAID1)
Daily Backup:
2:00 AM to backup server
Retention Policy:
1 year (365 days)
Deleted Items Retention:
14 days

## Monitoring & Maintenance
CPU Warning:
Alert if >70% sustained usage
Memory:
16GB allocated, 75% typical utilization
Disk Space:
Alert if <10% free space remains
Reboot Cycle:
Monthly maintenance window 2-4 AM Saturday
Test Connect:
Mail > File > Test Email AutoConfiguration


## Common Issues
Cannot Connect to Mail:
Verify EXCH01 status, check firewall, test DNS resolution
Full Mailbox:
Run Get-MailboxStatistics, advise user to archive old emails
Slow Email:
Check EXCH01 CPU/memory, disable ActiveSync if not needed


## File Server ##
## FILESERV01 Specifications
IP Address:
10.0.2.30
Location:
Server Room A
OS:
Server OS 2022 Standard
Total Storage:
50TB (RAID6, redundant drives)
Backup:
Daily at 2:00 AM to tape drive

## Standard Shares
\\FILESERV01\shared - Company-wide shared documents

\\FILESERV01\departments\Sales - Sales department files

\\FILESERV01\departments\Engineering - Engineering team files

\\FILESERV01\departments\Finance - Finance/Accounting files

\\FILESERV01\departments\Operations - Operations team files

\\FILESERV01\departments\Marketing - Marketing department files

\\FILESERV01\departments\Support - Customer Support department files

\\FILESERV01\departments\HR - HR department files

\\FILESERV01\departments\Legal - Legal department files

\\FILESERV01\departments\Facilities - Facilities department files

\\FILESERV01\departments\Executive - Executive department files

\\FILESERV01\departments\Accounting - Accounting department files

\\FILESERV01\departments\Design - Design team files

Restricted / Project Shares (access by security group, not department)
\\FILESERV01\Legal-Cases - Legal case files (access controlled by the "Legal Case Management" AD security group, NOT the Legal department group). If a Legal user gets "Access Denied" here while teammates can open it, add them to the "Legal Case Management" group in Directory - this is a group-membership issue, not a drive-mapping one.

## Mapped Drive Letters
H: = Personal home directory \\FILESERV01\users\{username}

S: = Shared \\FILESERV01\shared

D: = Department \\FILESERV01\departments\{dept}

(Mapped via device policy on login)

Note:
H: is the on-prem home drive (lives on FILESERV01, mapped via device policy). Cloud Drive is separate - cloud personal storage that syncs across devices. Both can hold personal files; H: is on-prem, Cloud Drive is in the cloud.

## Quotas & Limits
Per User Home:
100GB
Per Department:
500GB
Shared Folder:
Unlimited (monitored)
Backup Retention:
30 days of daily snapshots

## Access Troubleshooting
Cannot Access Share:
Check network connectivity, verify user in dept group, check share permissions
Slow File Copying:
Check network utilization, avoid large transfers during 2 AM backup
Drive Letter Not Mapping:
Restart computer, check device policy application (GPUPDATE /FORCE)
Disk Space Full:
Alert department manager, recommend archive to Cloud Drive or cleanup



## Print Server ##
## PRINT01 Specifications
IP Address:
10.0.2.40
Location:
Server Room B
OS:
Server OS 2022 Standard
Role:
Centralized print queue management
Management:
Print Management console (printmanagement.msc) on PRINT01, or \\PRINT01 share (restricted to IT)


## Troubleshooting
Printer Offline:
Check network cable, power cycle printer, check PRINT01 queue status
Cannot Connect / Wrong IP:
Printer IPs may change after network maintenance. Remove the old printer, look up the correct IP in the table above, and re-add via TCP/IP.
Driver Issues:
Reinstall Universal Print Driver, clear print spooler (restart PRINT01)
Slow Printing:
Check queue length, large file in queue, verify printer memory
Cannot Find Printer:
Verify PRINT01 is online, check floor location, manually add by IP address


