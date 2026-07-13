## Server Settings ##
Server:
mail.servicedesk-simulator.com
Port:
443
Encryption:
SSL/TLS
Username:
firstname.lastname@servicedesk-simulator.com
Password:
Domain password (same as your domain login)


## iOS: How to Navigate to Server Settings
1. Open Settings → Mail → Accounts

2. Tap the work email account

3. Tap "Account Settings" or the account email address

4. Under "Incoming Mail Server", update:

• Host Name: mail.servicedesk-simulator.com
• Port: 443 | SSL: ON
5. Tap Done and wait for the account to verify


## Android: How to Navigate to Server Settings
1. Open Settings → Accounts → Work email account

2. Tap "Account Settings" or "Server Settings"

3. Under "Incoming Server", update:

• Server: mail.servicedesk-simulator.com
• Port: 443 | Security Type: SSL/TLS
4. Tap Done/Save and allow the account to re-sync


## How to Instruct Users via Chat ##
When a user's email works on PC but not their phone, guide them through these steps via Chat:

1. First confirm the issue is device-specific. Ask: "Can you access your email on your laptop or webmail?"

2. If YES → server settings issue. Send them the correct server info above

3. Tell user: "Go to Settings → Mail/Accounts → tap your work email → Account/Server Settings"

4. Have them update the server to mail.servicedesk-simulator.com, port 443, SSL/TLS on

5. If NO (email doesn't work anywhere) → likely a password issue, reset in AD instead


## Common Troubleshooting ## 
Cannot Connect to Server:
Verify SSL/TLS is ON, check firewall allows 443, test on WiFi and cellular
Wrong Password Error:
Confirm email format (firstname.lastname@servicedesk-simulator.com), verify caps lock, try resetting password in AD
ActiveSync Disabled Error:
Contact helpdesk, may need to enable ActiveSync on mailbox in Mail Server
Certificate Warning:
Device may need SSL certificate update, try deleting account and re-adding