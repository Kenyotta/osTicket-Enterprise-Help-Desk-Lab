# System Configuration

## Purpose

After successfully deploying osTicket, the next phase focused on configuring the help desk to simulate a real-world enterprise IT support environment. This included organizing departments, defining user roles, creating Service Level Agreements (SLAs), and configuring ticket workflows.

These configurations transform a basic installation into a functional help desk capable of supporting day-to-day IT operations.

---

## Objectives

The objectives for this phase were to:

* Configure core help desk settings
* Create departments and teams
* Configure agent roles and permissions
* Create help topics
* Configure Service Level Agreements (SLAs)
* Test ticket creation and routing
* Validate administrative access

---

## Components Configured

### Departments

Departments separate tickets by function and responsibility.

Examples include:

* Help Desk
* Security Operations (SOC)
* Network Operations
* Human Resources

---

### Agent Roles

Agent roles determine the level of access each technician has within the system.

Examples include:

* Administrator
* Manager
* Support Technician
* Read-Only Analyst

Role-based permissions help enforce the principle of least privilege by granting users only the access required to perform their responsibilities.

---

### Help Topics

Help Topics simplify ticket submission by allowing users to categorize requests.

Examples include:

* Password Reset
* Software Installation
* Hardware Issue
* Network Connectivity
* Security Incident
* Access Request

---

### Service Level Agreements (SLAs)

SLAs define response and resolution expectations based on ticket priority.

Typical priority levels include:

| Priority | Example Response Time |
| -------- | --------------------- |
| Critical | 1 Hour                |
| High     | 4 Hours               |
| Normal   | 8 Hours               |
| Low      | 24 Hours              |

---

## Validation

After configuration, the following items were verified:

* Administrator access
* Agent access
* Department availability
* Help topic selection
* Ticket creation workflow
* Ticket assignment
* SLA functionality

---

## Lessons Learned

Configuring a help desk involves more than installing software. Proper planning of departments, permissions, and workflows is essential for efficient operations and secure access management.

This phase reinforced the importance of:

* Role-based access control
* Organized ticket categorization
* Standardized workflows
* Service management best practices
* Security through least privilege

---

## Outcome

The osTicket environment was successfully configured to support enterprise-style help desk operations. With departments, roles, SLAs, and ticket workflows in place, the lab now reflects the structure of a professional IT support environment and is ready for future integrations such as email automation, Active Directory, and SIEM platforms.
