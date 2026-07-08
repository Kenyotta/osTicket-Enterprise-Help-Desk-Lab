# osticket-helpdesk-lab
osTicket Enterprise Help Desk Lab
Overview

The osTicket Enterprise Help Desk Lab is a self-hosted IT support environment built on Ubuntu Server using the open-source osTicket platform. This project simulates a real-world enterprise help desk where users can submit support requests, technicians can manage incidents, and administrators can configure service workflows.

The purpose of this lab is to strengthen practical system administration, Linux, web server, database, and ticket management skills while building a professional cybersecurity and IT portfolio. As the project evolves, additional enterprise features such as automated email ticketing, Active Directory integration, and SIEM connectivity will be incorporated.

Objectives
- Deploy a production-style help desk environment
- Configure a complete LAMP stack (Linux, Apache, MariaDB, PHP)
- Install and configure osTicket
- Create and manage help desk departments, agents, and ticket workflows
- Practice Linux system administration and troubleshooting
- Document the deployment using professional technical documentation
- Prepare the environment for future SOC and cybersecurity integrations

Lab Environment
Component	       Technology
Operating System	Ubuntu Server 22.04 LTS
Web Server	       Apache 2
Database	       MariaDB
Programming Language	PHP 8.1
Help Desk Platform	osTicket v1.18.1
Virtualization	Oracle VM VirtualBox

Project Status

Current Phase: Core Help Desk Deployment

Completed
- Ubuntu Server deployment
- Apache installation and configuration
- PHP installation and required extensions
- MariaDB installation and database creation
- osTicket installation
- Initial web configuration
- Administrative dashboard access
- Project documentation

In Progress
- Email-to-ticket functionality
- Help desk workflow customization
- Department and agent configuration
- Knowledge base development
  
Planned
- Active Directory integration
- SIEM integration
- Security monitoring
- Incident response workflows
- Automation enhancements

This repository documents each stage of the deployment process, configuration changes, troubleshooting steps, and lessons learned throughout the project. The goal is to demonstrate practical IT support, Linux administration, and enterprise help desk skills through a fully documented hands-on lab.

## Skills Demonstrated

This project demonstrates hands-on experience with building, configuring, and troubleshooting an enterprise-style help desk environment.

Key skills practiced in this lab include:

* Linux server administration
* Apache web server configuration
* MariaDB database setup and management
* PHP application deployment
* osTicket installation and configuration
* Help desk ticket lifecycle management
* User, agent, department, and SLA configuration
* Cron job automation
* IMAP email integration troubleshooting
* Technical documentation
* Production-style service troubleshooting
* Cybersecurity lab planning

## Features

### Current Features

* Self-hosted osTicket help desk deployed on Ubuntu Server
* Apache web server hosting the application
* MariaDB database backend
* PHP-based web application
* Web-based agent and administrator dashboards
* Ticket creation and management
* Configurable departments and help topics
* Role-based access control for agents and administrators
* Service Level Agreement (SLA) support
* Cron job automation for scheduled maintenance tasks
* Professional project documentation and deployment guides

### Planned Features

* Email-to-ticket automation using Gmail IMAP
* Active Directory / LDAP authentication
* SIEM integration for security event tracking
* Automated ticket creation from security alerts
* Incident response workflows
* Knowledge base expansion
* Security monitoring dashboard


## Architecture

The osTicket Enterprise Help Desk Lab is built on a traditional LAMP stack and is designed to simulate a production-style IT support environment.


                    End Users
                         │
                         ▼
                Web Browser (HTTP)
                         │
                         ▼
              Ubuntu Server 22.04 LTS
                         │
        ┌────────────────┼────────────────┐
        │                │                │
        ▼                ▼                ▼
    Apache 2         PHP 8.1        Cron Service
        │                │                │
        └────────────┬───┘                │
                     ▼                    │
              osTicket v1.18.1 ◄──────────┘
                     │
                     ▼
               MariaDB Database
                     │
                     ▼
              Ticket Information

           (Future Enhancements)

 Gmail IMAP ─────────► Email-to-Ticket

 Active Directory ──► User Authentication

 SIEM Platform ─────► Automated Incident Tickets
```

### Architecture Overview

* **Apache** serves the osTicket web application to end users and support agents.
* **PHP** processes requests and communicates with the database.
* **MariaDB** stores ticket data, user accounts, departments, and system configuration.
* **Cron** executes scheduled background tasks and future automation jobs.
* **Future integrations** will include Gmail IMAP for automated email ingestion, Active Directory for centralized authentication, and SIEM platforms for security event ticket creation.


## Project Walkthrough

This project was completed in phases to mirror the deployment and configuration of a production-style help desk environment. Each phase is documented with configuration notes, screenshots, and troubleshooting details.

### Phase 1 – Environment Preparation

* Installed Ubuntu Server 22.04 LTS
* Updated the operating system
* Verified network connectivity
* Prepared the server for application deployment

### Phase 2 – LAMP Stack Deployment

* Installed Apache web server
* Installed PHP and required extensions
* Installed and secured MariaDB
* Verified all required services were operational

### Phase 3 – Database Configuration

* Created the osTicket database
* Created a dedicated database user
* Assigned appropriate database permissions
* Verified database connectivity

### Phase 4 – osTicket Installation

* Downloaded and extracted osTicket
* Configured Apache to host the application
* Completed the web-based installation
* Created the administrator account
* Verified access to the Agent and Admin panels

### Phase 5 – System Configuration

* Configured help desk settings
* Created departments and help topics
* Configured roles, permissions, and SLA plans
* Tested ticket creation and management

### Phase 6 – Troubleshooting

* Diagnosed email-to-ticket functionality
* Verified Gmail IMAP connectivity
* Tested cron job execution
* Documented findings and corrective actions

### Future Development

The lab will continue to expand with enterprise-focused features, including Active Directory integration, SIEM connectivity, automated incident creation, and additional security monitoring capabilities.

## Repository Structure

```text
osTicket-Enterprise-Help-Desk-Lab/
│
├── README.md                  # Project overview and documentation
├── LICENSE                    # Project license
│
├── docs/
│   ├── 01-environment-setup.md
│   ├── 02-lamp-stack.md
│   ├── 03-database-configuration.md
│   ├── 04-osticket-installation.md
│   ├── 05-system-configuration.md
│   ├── 06-troubleshooting.md
│   └── lessons-learned.md
│
├── screenshots/
│   ├── environment/
│   ├── lamp-stack/
│   ├── database/
│   ├── osticket-installation/
│   ├── system-configuration/
│   └── troubleshooting/
│
└── assets/
    └── architecture-diagrams/
```

### Documentation

* **README.md** provides a high-level overview of the project.
* **docs/** contains detailed deployment guides, configuration steps, and troubleshooting documentation.
* **screenshots/** stores evidence of each deployment phase and configuration milestone.
* **assets/** contains diagrams and supporting images used throughout the documentation.

## Screenshots

The following screenshots document the deployment and configuration of the lab. Additional screenshots will be added as new features and integrations are completed.

| Screenshot          | Description                                          |
| ------------------- | ---------------------------------------------------- |
| Ubuntu Server       | Initial Ubuntu Server installation and configuration |
| Apache & PHP        | Apache web server and PHP verification               |
| MariaDB             | Database creation and user configuration             |
| osTicket Installer  | Web-based installation wizard                        |
| Agent Dashboard     | Agent interface after successful installation        |
| Admin Panel         | Administrative dashboard                             |
| Ticket Management   | Example ticket lifecycle                             |
| Help Topics         | Help topic configuration                             |
| Departments         | Department configuration                             |
| SLA Plans           | Service Level Agreement configuration                |
| Roles & Permissions | Agent role configuration                             |
| Troubleshooting     | Email-to-ticket debugging and system logs            |

> **Note:** Screenshots are organized within the `screenshots/` directory and will continue to be updated as the project progresses.

## Future Enhancements

This project is designed to evolve into a complete enterprise IT support and cybersecurity lab. Planned enhancements include:

### Help Desk Improvements

* Complete Gmail IMAP email-to-ticket automation
* Expand departments, teams, and help topics
* Build a searchable knowledge base
* Create additional SLA policies and ticket workflows

### Identity & Access Management

* Integrate Active Directory / LDAP authentication
* Enable centralized user and group management
* Configure role-based access using domain accounts

### Security Operations

* Integrate a SIEM platform for centralized log collection
* Automatically generate tickets from security alerts
* Create incident response workflows
* Map security events to the MITRE ATT&CK framework

### Automation

* Expand cron-based maintenance tasks
* Automate ticket routing and assignment
* Develop custom scripts for system monitoring

### Documentation

* Add detailed deployment guides
* Publish troubleshooting and knowledge base articles
* Expand screenshots and architecture diagrams
* Document lessons learned and best practices throughout the project

## Project Status

**Status:** 🟡 Active Development

The core infrastructure for the osTicket Enterprise Help Desk Lab has been successfully deployed and is fully operational. The environment currently supports ticket creation and management through the web interface and serves as the foundation for future enterprise integrations.

### Current Progress

**Completed**

* Ubuntu Server deployment
* Apache web server configuration
* PHP installation and configuration
* MariaDB database deployment
* osTicket installation and initial configuration
* Administrative and Agent dashboard access
* Ticket creation and management
* Professional project documentation

**In Progress**

* Gmail IMAP email-to-ticket automation
* Help desk workflow optimization
* Expanded documentation and screenshots

**Upcoming Milestones**

* Active Directory / LDAP integration
* SIEM integration for security event monitoring
* Automated incident ticket generation
* Security monitoring and alert workflows
* Knowledge base development
* Additional automation and scripting

This repository will continue to be updated as new features are implemented and additional enterprise technologies are integrated into the lab.

Lessons Learned

Building this lab provided valuable hands-on experience beyond simply installing software. Throughout the deployment, I strengthened my understanding of Linux system administration, web application hosting, database management, and structured troubleshooting.

Some of the key takeaways from this project include:

- Planning the deployment before making configuration changes helps reduce troubleshooting time.
- Reading system logs and validating services step by step is more effective than guessing at solutions.
- Proper documentation makes it easier to reproduce deployments and resolve future issues.
- Enterprise applications depend on multiple services working together, including the operating system, web server, database, scheduled tasks, and network configuration.
- Not every issue has an immediate solution. Investigating, documenting findings, and testing different approaches are essential parts of real-world IT support.

This project reinforced the importance of methodical troubleshooting, documentation, and continuous learning—skills that are fundamental to both IT support and cybersecurity roles.
