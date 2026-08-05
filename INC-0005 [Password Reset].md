| Field       | Value                                                                                             |
| ----------- | ------------------------------------------------------------------------------------------------- |
| Ticket ID   | INC-0005                                                                                         |
| Priority    | P2 – High                                                                                |
| Category    | Identity & Access Management           |                                                                           
| Subcategory | Password Reset                  |                                                        
| Reported By | Chris Nguyen |
| Department  | Engineering                                                                                |Location     | Floor 1
                                                                     |
| Contact     | x6150                                                                                          |
| Assigned To | Aidan Baker – IT Support                                                                          |
| Status      | Resolved                                                                                          |


## User Report
The user returned from a two-week vacation and was unable to remember their account password. The user requested a temporary password reset to regain access to company systems and advised that they had several meetings scheduled within the next 15 minutes.

## Business Impact
The user was unable to access their workstation, Microsoft 365, email, Microsoft Teams, or other company resources. Failure to restore access promptly would prevent attendance at scheduled meetings and delay work.

## Resolution Process
1) Troubleshooting Performed - User attempted to recall their password without success.
User confirmed their manager had approved a password reset.
User was unable to recall their employee ID.
User remained unable to sign in.

2) Reviewed the reported issue and confirmed a password reset request had been received. As password resets require identity verification, no account changes were made until the user's identity could be confirmed.

3) Opened Active Directory and searched for the user's account using the username provided in the service request. Confirmed the account was active and ready for verification.

4) Sent a verification code to the user's registered contact method. Requested the user provide the code before proceeding with any account changes. Successfully verified the user's identity once the correct code was received.

5) Generated a temporary password within Active Directory and configured the account for secure access according to company password reset procedures. Opened Microsoft Teams and securely sent the temporary password to the verified user. Instructed the user to sign in immediately and create a new password when prompted. The user successfully authenticated using the temporary password, created a new permanent password and confirmed access to Microsoft 365, Outlook, Microsoft Teams.

Ticket Closed. INC-0005 Resolved.
