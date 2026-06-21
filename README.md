# osticket-helpdesk-lab
This project documents the deployment of a full osTicket-based IT Service Desk on an Ubuntu Linux server using Apache, MySQL, and PHP.  The goal was to simulate a real-world IT support environment used in enterprise service desks.

 osTicket Helpdesk Lab Deployment
 Project Overview

This project documents the deployment of a full osTicket-based IT Service Desk on an Ubuntu Linux server using Apache, MySQL, and PHP.

The goal was to simulate a real-world IT support environment used in enterprise service desks.

Technology Stack

Ubuntu Server
Apache2 Web Server
MySQL Database
PHP 8.x
osTicket v1.18.1

Installation Steps

1. System Update
sudo apt update && sudo apt upgrade -y
2. Install Apache, MySQL, PHP
sudo apt install apache2 mysql-server php libapache2-mod-php php-mysql -y
3. Install Required PHP Extensions
sudo apt install php-imap php-xml php-mbstring php-intl php-apcu -y
4. Deploy osTicket
Downloaded osTicket
Extracted to:
/var/www/html/osticket
5. Database Setup
Created MySQL database:
osticket
Configured root access for application
6. Web Installation

Accessed:

http://server-ip/osticket/setup

Completed:

Admin account creation
Database connection
System configuration

 Security Steps
 
Removed setup directory after installation:
sudo rm -rf /var/www/html/osticket/setup
Set correct file permissions:
sudo chmod 0644 include/ost-config.php

Features Implemented

Ticket creation system
Admin/staff dashboard
User portal
MySQL-backed ticket storage

Key Skills Learned

Linux file system navigation
Apache web hosting
MySQL database configuration
PHP web application deployment
Troubleshooting server permissions

Challenges Faced

File permission errors (403 Forbidden)
MySQL authentication issues
osTicket installation validation errors
PHP dependency resolution
