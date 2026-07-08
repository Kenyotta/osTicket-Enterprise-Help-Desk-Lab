# Database Configuration

## Purpose

This phase focused on configuring the MariaDB database required by osTicket. A dedicated database and user account were created to securely store application data, including tickets, users, departments, system settings, and knowledge base articles.

Using a dedicated database user instead of the administrative root account follows security best practices by limiting application permissions to only what is required.

## Database Environment

| Component       | Configuration       |
| --------------- | ------------------- |
| Database Server | MariaDB             |
| Database Name   | osticket            |
| Database User   | osticketuser        |
| Authentication  | Local Database User |

## Configuration Objectives

During this phase, the following tasks were completed:

* Verified the MariaDB service was running
* Accessed the MariaDB server
* Created the osTicket database
* Created a dedicated database user
* Assigned the required database permissions
* Applied privilege changes
* Verified database connectivity

## Security Considerations

The database was configured using a dedicated application account rather than the MariaDB root account. This approach improves security by limiting the application's permissions and reducing the potential impact of unauthorized access.

Key security practices implemented include:

* Separate application database
* Dedicated database user
* Limited database privileges
* Principle of least privilege
* Database access restricted to the local server

## Verification

Before continuing with the osTicket installation, the following items were confirmed:

* MariaDB service was operational
* The **osticket** database existed
* The application user was successfully created
* Database permissions were correctly assigned
* The database was ready for the osTicket installation wizard

## Outcome

The MariaDB environment was successfully configured and prepared for the osTicket installation. With the database infrastructure in place, the application could securely connect to its backend storage during the web-based installation process.
