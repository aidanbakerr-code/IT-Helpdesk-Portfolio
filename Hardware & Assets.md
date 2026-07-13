## Choosing a PC Setup ##
## When You Need This
A coworker needs a computer, either a new hire or a replacement for one that died. Before you set it up in Tools -> Computer Deployment, work out WHICH kind of setup that person needs. The wrong method means rebuilding the machine, so match the user to a profile first.

## The Three Deployment Methods
Cloud Identity Join:
Cloud-only. The device enrolls into Cloud Identity and Device Manager during first-time setup. Device Manager then pushes the security baseline, Office Suite and remote management automatically. This is the default for most office users.
Imaging Server:
Lays down the standardized corporate image over the network. The machine PXE-boots into an Imaging Server task sequence. Use it when the build needs legacy software or on-prem device policy that the cloud can't deliver. The Customer Support softphone is the classic case.
Manual Domain Join:
Configure the Workstation OS by hand and join it to the on-prem Directory domain. Use it for shared Facilities kiosks and Engineering lab/test machines that are not per-user cloud devices.

## Who Gets What
Standard office departments:
Cloud Identity Join
• Covers: Accounting, Design, Executive, Finance, HR, Legal, Marketing, Operations, Sales (and a regular Engineering laptop)
• Needs: Cloud Identity join, Device Manager enrollment, Office Suite, security baseline, remote management
• Why: Normal cloud-managed office users with no legacy or on-prem needs. This is the default path for roughly 80% of devices.
Customer Support:
Imaging Server
• Needs: legacy softphone software, on-prem device policies, VPN client during deployment
• Why: The support softphone and on-prem device policy cannot come from Device Manager, so the machine has to be imaged from Imaging Server.
Facilities:
Manual Domain Join
• Applies to: shared floor / kiosk workstations
• Needs: shared workstation, domain joined, auto-login kiosk account, label-printer software
• Why: A shared kiosk on the domain (print/log station, front desk, loading dock), configured by hand, not a per-user cloud device.
Engineering lab/test machines:
Manual Domain Join
• Needs: manual setup, NOT enrolled in Device Manager, isolated network, custom software only
• Why: Lab and test boxes are deliberately kept off the managed fleet, so they are configured by hand with no cloud enrollment. (A regular Engineering laptop is still a standard Cloud Identity Join; only the lab/test machines are manual.)

## Quick Decision Guide
1) Standard cloud-managed office user (Accounting, Design, Executive, Finance, HR, Legal, Marketing, Operations, Sales, or a regular Engineering laptop)? Use Cloud Identity Join.
2) Customer Support agent who needs the legacy softphone and on-prem device policy? Use Imaging Server.
3) Shared Facilities kiosk, or an Engineering lab/test box? Use Manual Domain Join.

## Signing In After Setup
When the imaged or domain-joined machine reboots to the sign-in screen, it does NOT pre-fill an account; it lands on "Other user," exactly like a real domain workstation. Sign in with your domain credentials: your display name as the user name, and the shared domain password Servicedesk2026!.

## After You Build It
A finished PC goes onto the shelf as stock, tracked by its setup type (Cloud Identity, Imaging Server, or Manual). When a replacement ticket comes in (for example, a user whose PC has fully died), ship the matching in-stock PC from Ship Manager. If none of that type is built yet, set one up in Computer Deployment first, then ship it.

## Standard Desktop Configuration
## Desktop Specification (Current Standard)
Processor:
Core i7 processor (8-core, 3.6GHz base)
RAM:
16GB DDR4-3200 (2x8GB, upgradeable to 32GB)
Storage:
512GB NVMe SSD (M.2 PCIe 4.0) in RAID 1
Motherboard:
Proprietary, integrated TPM 2.0
Power Supply:
500W 80+ Bronze
Peripherals & Connections
Monitors:
Dual SD ClearView 24" (1920x1200, IPS, USB-C dock)
Video Output:
2x DisplayPort (primary monitor), 1x HDMI (secondary)
Audio:
3.5mm headphone jack, USB speaker/headset support
Network:
1Gbps Ethernet RJ45, WiFi 6E (onboard)
USB:
4x USB 3.1, 2x USB 2.0, 1x USB-C (DisplayPort alt-mode)
Naming Convention
Format:
SD#### (SD followed by four digits)
Examples:
SD1042, SD1043, SD2001
Asset Tag:
Sticker on back of monitor (track in IT system)
Serial Number:
Service tag (bottom of tower)
OS & Software
Operating System:
Workstation OS Enterprise 23H2 (fully patched)
Office Suite:
Pre-installed and licensed
Antivirus:
the built-in antivirus (managed, auto-update)
VPN:
VPN client (pre-configured, no setup needed)
Printer Drivers:
Universal Print Driver (pre-installed)
Maintenance
Annual:
HW check, SSD health check, RAM test
OS Updates:
Monthly Patch Tuesday (reboots scheduled)
Lifecycle:
4-5 years typical, refresh around year 5
Recycling:
Assets collected at end-of-life, data wiped, sent to certified recycler

## Laptop Specification (Current Standard)
Processor:
Core i7 processor (10-core, 3.3GHz, P+E cores)
RAM:
16GB LPDDR5 (soldered, not upgradeable)
Storage:
512GB M.2 SSD (PCIe 4.0, fast, expandable via SD card)
Battery:
63Wh (up to 12 hours real-world usage)
Weight:
1.78 kg (3.9 lbs)

## Display & Connectivity
Display:
15.6" FHD (1920x1080) IPS anti-glare
WiFi:
WiFi 6E (onboard, dual-band + 6GHz)
Bluetooth:
5.3 (for headsets, mice, keyboards)
Ethernet:
USB-C 2.5Gbps adapter (optional)
Ports:
2x Thunderbolt 4, 2x USB 3.2, audio jack, microSD reader

## Docking Station (Included for Remote Workers)
Model:
SD Dock Pro Docking Station
Connections:
1x Thunderbolt 3 cable (single-cable dock)
Output:
Dual 4K@60Hz monitors OR 1x 6K@60Hz
USB Ports:
7x USB 3.0 + 2x USB-C charging
Ethernet:
1Gbps RJ45 (for cable alternative)
Charging:
130W power supply (charges laptop + peripherals)

## Naming Convention
Format:
SD#### (SD followed by four digits)
Examples:
SD1042, SD1043, SD2001
Asset Tag:
Bottom of laptop (track in IT system)
Serial Number:
Service tag (System Information)

## OS & Software
Operating System:
Workstation OS Enterprise 23H2
Office Suite:
Pre-installed and licensed
VPN Client:
Pre-configured for remote access
Encryption:
Drive Encryption enabled (whole-disk encryption)
Antivirus:
the built-in antivirus

## Remote Worker Setup
Standard equipment:
SD Laptop Pro + SD Dock Pro + dual monitors + USB peripherals
Shipped in:
Secure packaging to home address
Setup:
Pre-configured, user just plugs in ethernet + power
VPN:
Auto-connects on startup OR click in system tray
Backup:
Cloud Drive configured for automatic file sync
Support:
Remote helpdesk support available during business hours


## Company-Provided Standard Peripherals
Keyboard:
SD KB100 (USB or wireless) - included with desktop
Mouse:
SD MS100 (USB or wireless) - included with desktop
Headset:
Optional (request via IT, approved headset models)
USB Hub:
Powered USB 3.0 hub required if more than 4 devices
Cost:
All company-provided peripherals, no user cost

## Personal USB Devices (Allowed with Restrictions)
Mice & Keyboards:
Yes, allowed and supported
External Drives:
NO - security/compliance policy (DLP blocking)
USB Hubs:
Only powered hubs recommended (unpowered drains laptop power)
Thumb Drives:
NO - use Cloud Drive instead (cloud storage)
Phone Charging Cables:
Yes, personal cables OK, use any USB adapter

##USB Hub Requirements
Type:
Powered USB 3.0 hub (requires external power adapter)
Minimum:
4x USB 3.0 ports, 1x power input
Max Devices per Hub:
4 devices recommended (bandwidth sharing)
Cable Quality:
Use certified USB 3.0 cables (avoid cheap knockoffs)
Power Adapter:
2+ amps recommended to avoid brownouts

## Security Policy
No DLP (Data Loss Prevention) Bypass:
Cannot copy files to personal USB devices
Rationale:
Proprietary info protection, IP confidentiality
Compliance:
Company policy enforced by device policy
Alternative:
Use Cloud Drive, Team Sites, or Chat for file sharing

## Troubleshooting
Keyboard/Mouse Lag:
Check USB power (keyboard lights dim = low power), move hub away from WiFi
USB Device Not Recognized:
Try different USB port, restart computer, update drivers
Slow File Transfer:
Check USB 3.0 vs 2.0 (3.0 much faster), verify hub powered
Device Disconnects:
Check cable quality, move hub closer, use powered hub


## Monitor Setup 
## Monitor Specifications
Model:
SD ClearView Professional 24"
Resolution:
1920x1200 (16:10 aspect ratio, more vertical space)
Panel Type:
IPS (in-plane switching, wide viewing angles)
Brightness:
300 nits (bright for office)
Contrast:
1000:1 native
Response Time:
5ms zinc-to-gray
Port Type:
DisplayPort 1.4 + HDCP 2.2 support

## Multi-Monitor Configuration (Standard 2 Monitors)
Primary Monitor:
DisplayPort (higher refresh rate)
Secondary Monitor:
HDMI or DisplayPort (identical SD ClearView 24")
Resolution Each:
1920x1200 (both same)
Total Real Estate:
3840x1200 pixel workspace
Arrangement:
Side-by-side (desktop spanning across both)

## Connection Instructions
Desktop Setup:
1. Connect Primary to GPU DisplayPort #1

2. Connect Secondary to GPU DisplayPort #2 OR HDMI

3. Connect audio jack (headphone output) to monitor speakers (optional)

4. Power on both monitors

5. The Workstation OS auto-detects (Settings > Display > Multiple displays)

Laptop + Docking:

1. SD Dock Pro supports 2x monitors

2. Connect monitors to Thunderbolt 4 dock

3. Laptop connection via single USB-C cable

4. Automatic resolution detection (extend display)

## Troubleshooting
Monitor Won't Wake: Check power, monitor sleep setting (power button), press any key on keyboard

Flickering or Distortion:
Update the graphics driver, try different cable, restart computer
One Monitor Blank:
Check cable connection, verify in Display Settings that monitor is detected, right-click desktop > Display settings
Wrong Resolution:
Right-click desktop > Display settings > Set to 1920x1200 (native)
Second Monitor Not Detected:
Try DisplayPort instead of HDMI, update monitor firmware, restart computer