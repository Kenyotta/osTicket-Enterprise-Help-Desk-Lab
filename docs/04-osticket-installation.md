# osTicket Installation

## Purpose

This phase focused on deploying the osTicket application onto the configured LAMP environment. After preparing the operating system, web server, PHP environment, and database, the application was installed and configured through the web-based installation wizard.

The successful deployment of osTicket established a fully functional help desk platform capable of managing support requests, users, agents, and administrative settings.

---

## Installation Objectives

The goals of this phase were to:

* Download the latest supported version of osTicket
* Deploy the application to the Apache web server
* Configure the application directory
* Set appropriate file permissions
* Complete the web-based installation wizard
* Connect osTicket to the MariaDB database
* Create the initial administrator account
* Verify successful application deployment

---

## Deployment Process

The deployment process included:

* Downloading the osTicket installation package
* Extracting the application files
* Copying the application into the Apache web directory
* Configuring the required application files
* Assigning the correct ownership and permissions
* Restarting Apache to apply configuration changes

---

## Web Installation

After the application files were deployed, the browser-based installation wizard was used to complete the installation.

Configuration included:

* Help Desk Name
* Administrator Account
* Administrator Email Address
* Default System Email
* Database Host
* Database Name
* Database Username
* Database Password

After validation, the installer created the required database tables and generated the application configuration file.

---

## Post-Installation Tasks

After installation, several security and verification tasks were completed:

* Verified Agent Panel access
* Verified Admin Panel access
* Confirmed successful database connectivity
* Removed unnecessary installation files
* Secured the application configuration file
* Confirmed Apache was serving the application correctly

---

## Verification

The installation was considered successful after confirming:

* The osTicket login page loaded successfully.
* Administrator authentication functioned correctly.
* The Agent Dashboard was accessible.
* The Admin Panel loaded without errors.
* Ticket creation functionality was available.
* Database communication was successful.

---

## Outcome

The osTicket platform was successfully deployed and integrated with the existing LAMP stack. The environment was now capable of supporting help desk operations and provided the foundation for additional configuration, workflow customization, and future cybersecurity integrations.
