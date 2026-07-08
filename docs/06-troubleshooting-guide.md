# Troubleshooting Guide

## Purpose

Throughout the deployment of the osTicket Enterprise Help Desk Lab, several configuration and deployment issues were encountered. Each issue was investigated using a structured troubleshooting process to identify the root cause, implement a solution, and verify successful resolution.

Documenting these issues creates a reusable knowledge base and demonstrates a methodical approach to diagnosing technical problems.

---

# Troubleshooting Methodology

Every issue was approached using the following process:

1. Identify the problem.
2. Collect relevant error messages and logs.
3. Verify the current system configuration.
4. Isolate the root cause.
5. Apply the appropriate fix.
6. Test the solution.
7. Document the outcome.

---

# Issue 1 – Apache Returned a 404 Error

### Symptoms

* The osTicket webpage displayed a **404 Not Found** error.
* Apache was running, but the application could not be accessed.

### Investigation

The Apache service was verified first to confirm the web server was operational.

The application directory and document root were then inspected to ensure the osTicket files were located in the expected location.

### Resolution

The web server configuration was reviewed and corrected so Apache pointed to the proper application directory.

### Result

The osTicket installation page loaded successfully.

---

# Issue 2 – Database Connection Verification

### Symptoms

The application required a successful connection to MariaDB before installation could continue.

### Investigation

The database service was verified.

Database credentials and permissions were reviewed.

The application database was confirmed to exist.

### Resolution

Database connectivity was validated before continuing with the installation wizard.

### Result

The installer successfully connected to MariaDB.

---

# Issue 3 – Configuration File Permissions

### Symptoms

The installer reported issues writing the application configuration file.

### Investigation

Linux file ownership and permissions were reviewed.

### Resolution

The required permissions were temporarily adjusted to allow osTicket to generate the configuration file.

After installation, the configuration file was secured using appropriate permissions.

### Result

The installation completed successfully while maintaining security best practices.

---

# Issue 4 – Gmail IMAP Email Fetching

### Symptoms

* Gmail successfully accepted the IMAP connection.
* Scheduled cron jobs executed normally.
* Email messages were not converted into tickets.

### Investigation

The following items were verified:

* Gmail IMAP connectivity
* PHP IMAP extension
* Cron execution
* Email account configuration
* Mail server connectivity

An SSL/TLS handshake using OpenSSL confirmed successful communication with Gmail.

### Current Status

The environment successfully establishes an IMAP connection, but automated email retrieval is still under investigation.

This issue remains open and will continue to be documented as additional testing is completed.

---

# Lessons Learned

Several important troubleshooting principles were reinforced during this project:

* Verify basic services before investigating application-level problems.
* Read system logs before making configuration changes.
* Change one configuration at a time.
* Test after every modification.
* Document both successful and unsuccessful troubleshooting steps.
* Not every issue is resolved immediately—systematic investigation is part of professional IT operations.

---

# Conclusion

Troubleshooting was an essential part of this project and significantly strengthened practical Linux administration, web application support, and problem-solving skills. Rather than avoiding deployment challenges, each issue was investigated, documented, and used as a learning opportunity to improve future system administration practices.
