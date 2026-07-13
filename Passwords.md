## Password Policy ##
## Requirements ##
Minimum Length:
12 characters
Complexity:
MUST include uppercase + lowercase + number + special character
Special Characters:
!@#$%^&*()_+-=[]{}|;:,.<>?
Username:
Cannot contain username or reverse of username
Spaces:
Not allowed

## Expiration & History ##
Password Expiration:
90 days
Warning Notification:
User notified 14 days before expiration
Password History:
Last 12 passwords remembered (cannot reuse)
Lockout After Failed Attempts:
5 failed attempts within 15 minutes
Auto-Unlock: 30 minutes OR IT admin manual unlock after identity verification

# Lockout Rules ##
Failed Attempts Threshold:
5 failed login attempts
Time Window:
15 minutes (attempts must be within 15 min window)
Auto-Unlock Time: 30 minutes after lockout
Status:
Locked accounts show in Directory

## How to Unlock Manually ##
Verify Identity First:
Send verification code to registered phone in AD, confirm employee ID + department + manager name
Open Directory Users and Computers (DC01/DC02)

Find user account > Unlock account checkbox
Click OK
Inform user:
Password still same, only unlock applied
Never skip identity verification even if caller claims urgency

## Prevention ##
Advise users to:
Use strong password, store in password manager, wait 30 min before retry
Common Causes:
Caps lock on, wrong domain/email format, keyboard layout issue
Help Desk Tip:
Check EventViewer on DC01 for failed login attempts before unlocking