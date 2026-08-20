| Field       | Value                                                                                             |
| ----------- | ------------------------------------------------------------------------------------------------- |
| Ticket ID   | INC-0007                                                                                         |
| Priority    | P2 – High                                                                                |
| Category    | Identity & Access Management         |                                                                           
| Subcategory | Shared Folder Permissions                  |                                                        
| Reported By | Emily Carter |
| Department  | Marketing                                                                              |Location     | Floor 2
                                                                     |
| Contact     | x6185                                                                                         |
| Assigned To | Aidan Baker – IT Support                                                                          |
| Status      | Resolved                                                                                          |

##User Report

The user reported that they were unable to access the Marketing department's shared network folder. The user received an "Access Denied" message when attempting to open the folder.

The user confirmed that other members of the Marketing department were able to access the folder successfully.

##Business Impact

The user was unable to access marketing documents and shared resources required for their daily duties. The issue prevented the user from accessing department files and could delay ongoing Marketing activities.

##Resolution Process

1) Troubleshooting Performed - User confirmed that they were able to sign into their workstation normally.

User confirmed that they could access other network resources.

User confirmed that the Marketing shared folder was visible but returned an "Access Denied" message when opened.

2) Reviewed the reported issue and confirmed that the shared folder was online and accessible to other authorised Marketing users.

Confirmed that the issue was related to the user's access permissions rather than network connectivity.

3) Opened Active Directory and searched for the user's account.

Confirmed that the user's account was active and that authentication was functioning normally.

Reviewed the user's Active Directory security group memberships.

4) Identified the security group responsible for providing access to the Marketing shared folder.

Compared the affected user's group membership with another authorised Marketing employee.

The affected user was not a member of the required security group.

5) Confirmed that the user required access to the shared folder as part of their job responsibilities and that the appropriate access request had been authorised.

Added the user to the required Active Directory security group according to company access-control procedures.

6) Requested that the user sign out of Windows and sign back in so that the updated Active Directory group membership could be applied to their user session.

7) User signed back into Windows and successfully accessed the Marketing shared folder.

Confirmed that the user could open the required documents.

No additional permissions were granted beyond those required for the user's role.

Ticket Closed. INC-0008 Resolved.