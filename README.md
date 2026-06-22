# osticket-helpdesk-lab
osTicket Help Desk + Email-to-Ticket SOC Lab (Ubuntu 22.04 + Gmail IMAP)

       Project Overview

This project is a self-hosted IT help desk built using osTicket v1.18.1 on an Ubuntu 22.04 server. It simulates a real-world service desk environment and is being extended into a SOC-style lab with email ingestion, ticket automation, and future SIEM integration.

The goal is to practice:

IT support workflows
Ticket lifecycle management
Email ingestion via IMAP (Gmail)
Linux server administration
Cron automation
Debugging production-style service issues

      Architecture
 
User Email (Gmail IMAP)
        ↓
osTicket Mail Fetcher (IMAP 993)
        ↓
Apache Web Server (Ubuntu 22.04)
        ↓
PHP 8.1 + osTicket v1.18.1
        ↓
MySQL 8.0 Database (osticket schema)
        ↓
Ticket Storage + Agent Dashboard

    Tech Stack

Ubuntu Server 22.04 (Oracle VM)
Apache 2.4
PHP 8.1
MySQL 8.0
osTicket v1.18.1
Gmail IMAP (imap.gmail.com:993 SSL)
Cron (system scheduler)

   Email Configuration
 
Email Account: Gmail (IMAP)
Host: imap.gmail.com
Port: 993
Protocol: IMAP SSL
Auth Type: Basic Authentication (App Password recommended)
Fetch Interval: 5 minutes
Folder: INBOX

   Cron Configuration

System cron is configured to run osTicket tasks:

*/2 * * * * /home/ubuntu/siem_watch.sh
*/5 * * * * php /var/www/html/osticket/api/cron.php

   Cron service status:
Active and running 
Executes successfully 

    System Validation

Database:
MySQL running 
Tickets being created 
Web Server:
Apache operational 
SCP interface accessible 
Email Fetching:
IMAP connection verified  (Gmail TLS handshake successful)
Mail fetch pipeline currently not executing 

      Observed Issue
Email-to-Ticket Not Triggering
Despite valid configuration:

Email account is active
IMAP connection succeeds
Cron executes without errors

    However:

No email logs generated
No tickets created from email
MailFetcher does not appear to execute during cron run

   Troubleshooting Summary

 Completed steps:

Verified Gmail IMAP connectivity via openssl s_client
Confirmed cron execution
Verified database schema and email account configuration
Confirmed PHP IMAP extension installed
Tested manual cron execution (no output)
Confirmed tickets are being created via manual sources (Phone)

       Current Status
Apache	 Working
MySQL	Working
osTicket UI	 Working
Ticket Creation	 Working
Cron Jobs	 Running
Gmail IMAP	 Connected
Email Fetching	 Not executing
MailFetcher	 Not triggered
    
    Next Steps (Planned)
Fix MailFetcher execution flow
Validate osTicket cron task routing
Confirm email pipeline triggers
Integrate logging for email ingestion
Prepare SIEM forwarding (future phase)
Add forensic logging dashboard

   Learning Outcomes
Linux server setup and service debugging
IMAP email integration concepts
Cron automation behavior in Linux
PHP-based application debugging
MySQL schema inspection
Real-world help desk architecture design

     Project Status
Partially operational — core help desk works, email ingestion layer under investigation
