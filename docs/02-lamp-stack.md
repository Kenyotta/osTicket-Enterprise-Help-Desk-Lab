# LAMP Stack Installation

## Purpose

The second phase of the project focused on deploying the LAMP stack, which provides the foundation required to host the osTicket web application. The LAMP stack consists of Linux, Apache, MariaDB, and PHP, working together to deliver a secure and reliable web application environment.

## Components Installed

| Component | Purpose                                                          |
| --------- | ---------------------------------------------------------------- |
| Apache 2  | Hosts the osTicket web application                               |
| PHP 8.1   | Processes server-side application logic                          |
| MariaDB   | Stores ticket data, user accounts, and configuration information |

## Apache Installation

Apache was installed and configured as the primary web server for the project.

### Verification

After installation, the Apache service was verified to ensure it was running correctly and configured to start automatically during system boot.

## PHP Installation

PHP and the required extensions were installed to support the osTicket application.

The installation included the modules necessary for:

* Database connectivity
* XML processing
* IMAP email support
* Internationalization
* Multibyte string handling
* File management

### Verification

The installed PHP version and required extensions were verified before proceeding with the application deployment.

## MariaDB Installation

MariaDB was installed to provide the backend database used by osTicket.

Following installation, the database service was verified to ensure it was operational before creating the application database.

## Service Verification

Each service was confirmed to be operational before moving to the next deployment phase.

| Service | Status      |
| ------- | ----------- |
| Apache  | Operational |
| PHP     | Operational |
| MariaDB | Operational |

## Outcome

The LAMP stack was successfully deployed and verified. The environment was now prepared to host the osTicket application and support future configuration tasks.
