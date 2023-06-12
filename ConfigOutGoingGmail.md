## Config Outgoing Gmail

- Odoo -> Setting -> Developer Tool -> Developer mode
- Odoo -> Setting -> Navigation bar -> Technical -> Email Outgoing Mail Servers

### Outgoing Mail Servers

- Create A New OutGoing Server With:
  - Description: GmailServer/AnyNameNotEmpty
  - SMTP Server: smtp.gmail.com
  - SMTP Port: 465
  
  - Authenticate with: Username
  - Connection Security: SSL/TLS
  - Username: Your-Email-Address
  - Password: Apply a Google App Password ([Generate here](https://myaccount.google.com/apppasswords))

### Generate a Google App Password

1. Login to Your Google Account
2. Connect to the link: [https://myaccount.google.com/apppasswords](https://myaccount.google.com/apppasswords)
3. Create a New App Password
   - Select app: Mail
   - Select device: Windows
   - Press the "GENERATE" button
4. Note down the generated app password
![image](https://github.com/ChungChiuHung/docker.odoo15/assets/52248840/6872820f-1a14-4bfa-9747-db3427b52cd2)
