| Field       | Value                                                                                             |
| ----------- | ------------------------------------------------------------------------------------------------- |
| Ticket ID   | INC-0002                                                                                          |
| Priority    | P2 – High                                                                                    |
| Category    | Identity & Access Management              |                                                                           
| Subcategory | Multi-Factor Authentication (MFA)                    |                                                        
| Reported By | Laura Santos |
| Department  | Finance                                                                                  |
| Location    | Floor 1                                                                         |
| Contact     | x4080                                                                                            |
| Assigned To | Aidan Baker – IT Support                                                                          |
| Status      | Resolved                                                                                          |


## User Report
"I can't log in. I keep putting in the code from the app on my phone but it tells me it's wrong every time. The codes look right."

## Business Impact
Finance employee unable to authenticate using MFA and completely locked out of all company systems. User is unable to access Microsoft 365, email, financial applications, or shared resources, preventing them from carrying out their daily responsibilities.

## Resolution Process
1) Troubleshooting Review - the following checks had already been completed by the user:
Entered multiple verification codes from the Microsoft Authenticator app.
Restarted mobile phone.
Confirmed the latest code was being entered before it expired.
Issue persisted after several attempts.

2) Opened Active Directory from the administration console and searched for Laura Santos to verify the account was active and identify the associated user profile.

3) Opened Microsoft Teams and contacted the user's manager to confirm that an MFA reset was authorised and required before making any changes to the user's account.

4) Received confirmation from the manager that the MFA reset should proceed. Once approval was verified, continued with the account recovery process.

5) Within the Active Directory administration console, selected the user's account and performed an MFA Reset, clearing the existing multi-factor authentication registration and allowing the user to complete a new enrolment.

6) The user successfully signed in to their account and completed the MFA re-enrolment process using the Microsoft Authenticator application. Confirmed the user was able to access company resources and appeared online in Microsoft Teams. Contacted the user through Microsoft Teams to confirm that authentication was functioning correctly and that all required systems were accessible.



Ticket Closed. INC-0002 Resolved.
