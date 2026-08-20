| Field       | Value                                                                                             |
| ----------- | ------------------------------------------------------------------------------------------------- |
| Ticket ID   | INC-0006                                                                                         |
| Priority    | P2 – High                                                                                |
| Category    | Network & Connectivity           |                                                                           
| Subcategory | DNS/DHCP                  |                                                        
| Reported By | Sarah Williams |
| Department  | Finance                                                                               |Location     | Floor 1
                                                                     |
| Contact     | x6142                                                                                         |
| Assigned To | Aidan Baker – IT Support                                                                          |
| Status      | Resolved                                                                                          |

##User Report

The user reported that their workstation was connected to the company network but they were unable to access websites or several internal company resources. The user advised that other employees in the department were able to access the network normally.

##Business Impact

The user was unable to access websites, internal network resources and systems required to perform their daily duties. The issue was affecting a single employee but required prompt resolution to prevent disruption to the Finance department.

##Resolution Process

1) Troubleshooting Performed - User confirmed that their network cable was connected and that the workstation displayed an active network connection.

User confirmed that other employees were able to access the internet and internal resources.

User was unable to access websites using normal domain names.

2) Reviewed the reported issue and confirmed that the problem appeared to be isolated to the user's workstation. Tested the user's connection to the local network and confirmed that the workstation was physically connected.

3) Opened Command Prompt and ran ipconfig /all to review the workstation's IP configuration. Checked the assigned IPv4 address, subnet mask, default gateway and DNS server information.

The workstation was found to have an incorrect network configuration.

4) Tested connectivity to the default gateway using ping. The workstation was able to communicate with the local gateway.

Tested DNS resolution using nslookup and confirmed that domain-name resolution was failing.

5) Released and renewed the workstation's DHCP lease using:

ipconfig /release
ipconfig /renew

The workstation received a valid IP address, default gateway and DNS configuration.

6) Cleared the local DNS cache using:

ipconfig /flushdns

Tested DNS resolution again using nslookup and confirmed that domain names were resolving correctly.

7) Tested access to internal company resources and external websites. The user was able to access the required resources successfully.

The user confirmed that internet connectivity had been restored and that they could continue working normally.

Ticket Closed. INC-0006 Resolved.