## Network Architecture ##
## Network Subnets
Corporate Workstations:
10.0.1.0/24 (up to 254 devices)
Servers & Infrastructure:
10.0.2.0/24 (DC01, EXCH01, FILESERV01, etc.)
WiFi Clients:
10.0.3.0/24 (company WiFi devices)
Guest Network:
192.168.1.0/24 (visitor access, internet-only)

## Core Equipment
Core Router:
10.0.0.1 (gateway for all traffic)
Floor 1 Switch:
10.0.1.1 (connects desks on Floor 1)
Floor 2 Switch:
10.0.2.1 (connects desks on Floor 2)
Floor 3 Switch:
10.0.3.1 (connects desks on Floor 3)
Main Firewall:
10.0.0.254 (monitors inbound/outbound traffic)

## DNS & DHCP
Primary DNS:
10.0.2.10 (DC01)
Secondary DNS:
10.0.2.11 (DC02)
DHCP Server:
DC01 (10.0.2.10; serves the 10.0.1.x workstation scope)
DHCP Lease Time:
8 hours
Reserved IP Ranges:
Per VLAN, managed by IT

## ISP Connection
Provider:
Metro ISP
Connection Type:
Fiber optic, 1Gbps symmetrical
Gateway:
10.0.0.1 (external IP managed by ISP)
Support:
Call Metro ISP at 1-888-812-2591 for outages


##Remote Worker Home Network Issues
If remote worker has NO internet at all (not just VPN):
1. Have user restart their modem/router (unplug 30 seconds)

2. Wait 2-3 minutes for connection to re-establish

3. Have user restart their computer

4. Verify internet works, then reconnect VPN


## Wifi Networks ##
## SDSim-Secure (Corporate)
Type:
WPA2-Enterprise
Network Security Key:
ServiceDesk2026!
Auto-Join: Yes for domain-joined machines
Manual:
Select SDSim-Secure from available networks, enter key
IP Range:
10.0.3.0/24 (WiFi subnet)
Access:
All company resources (file shares, Mail Server, printers)
Coverage:
All offices and lobbies

## SDSim-Guest (Visitor)
Type:
WPA2 with password
Password:
Welcome2SDSim!
IP Range:
192.168.1.0/24 (guest subnet)
Session Duration:
24 hours (must reconnect daily)
Access:
Internet only (NO internal file shares, NO printers, NO Mail Server)
Speed:
Throttled to 10Mbps per device
Coverage:
Lobby, meeting rooms, cafeteria

##Troubleshooting
SDSim-Secure Won't Connect: Forget network, reconnect with key "ServiceDesk2026!"
Only One User Affected:
Forget network → reconnect with key
Guest Network Slow:
Verify speed tier, check device limit (many guests = slower)
Can't Connect to Resources: Check correct SSID (Secure vs Guest), verify IP range (10.0.3.x vs 192.168.1.x)
Password Wrong:
Guest password is case-sensitive "Welcome2SDSim!"
Connectivity Drops:
Move closer to AP, check signal strength (-50dBm or higher)

## DNS & DHCP ##
## DNS (Domain Name System)
Primary DNS:
10.0.2.10 (DC01 - Directory Integrated DNS)
Secondary DNS:
10.0.2.11 (DC02 - backup, automatic replication)
Query Process:
Device asks primary DNS for servicedesk-simulator.com, falls back to secondary if primary unavailable
Internal Domains:
servicedesk-simulator.com, internal.servicedesk-simulator.com
Public IP Resolution:
Metro ISP provides external DNS fallback

## DHCP (Dynamic Host Configuration Protocol)
DHCP Server:
DC01 (10.0.2.10)
Scope Distribution:
Workstations:
10.0.1.20 to 10.0.1.250
Servers:
10.0.2.30 to 10.0.2.250 (servers use static IPs)
WiFi Clients:
10.0.3.20 to 10.0.3.250
Lease Time:
8 hours (devices renew after 4 hours)
Gateway:
10.0.0.1 (next hop for external traffic)

##Troubleshooting
No IP Address:
Device not reaching DHCP (check ethernet cable, run 'ipconfig /release /renew')
Wrong Subnet:
If 169.254.x.x (APIPA), DHCP server down, restart DC01
DNS Not Resolving:
Run 'nslookup servicedesk-simulator.com', check DNS servers (ipconfig /all)
Slow Network:
Check DHCP lease renewal, excessive broadcasts, contact Tier 2


## VPN Client Overview
Client:
the VPN client (pre-installed on company laptops)
Portal:
vpn.servicedesk-simulator.com
Authentication:
Domain username + password + MFA approval
Access Grants:
File shares, internal apps, printers, email

## Setup Instructions
1. Open the VPN client app (bottom right taskbar tray)

2. Click Connect (or add portal: vpn.servicedesk-simulator.com if needed)

3. Sign in with domain credentials (firstname.lastname@servicedesk-simulator.com)

4. Approve MFA push notification on phone

5. Wait for "Connected" status

6. Access internal resources: \\FILESERV01\shared, etc.

##Download & Installation
Download Client:
https://vpn.servicedesk-simulator.com/portal
Extract .zip file

Run setup.exe (requires admin password)

Restart recommended

The VPN client appears in system tray

## Connection Issues
Cannot Connect:
Check internet, verify domain credentials, restart computer
MFA Not Appearing:
Check phone is reachable, try "Enter Passcode" option
Slow Speed on VPN:
Expected (encrypted tunnel), check internet speed, avoid large file transfers
Disconnects Frequently:
Check WiFi signal, disable WiFi power save, update client to latest version
Lost Access:
Contact helpdesk, may need to re-enroll or reset MFA