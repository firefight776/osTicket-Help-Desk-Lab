# osTicket Help Desk Lab

## Project Overview

This project documents the deployment, configuration, and administration of an osTicket help desk environment using Windows, XAMPP, Apache, PHP, and MariaDB.

The lab simulates a small enterprise IT support environment by demonstrating department and agent management, Role-Based Access Control (RBAC), ticket management, and common administrative tasks performed by Help Desk Technicians and Systems Administrators.

## Technologies & Environment

This lab was deployed on a Windows 11 workstation using XAMPP as the local web server environment. Apache hosted the osTicket web application while MariaDB stored ticket data. phpMyAdmin was used to create and manage the database throughout the deployment.

| Technology | Purpose |
|------------|---------|
| Windows 11 | Host operating system |
| XAMPP | Local web server stack |
| Apache | Web server hosting osTicket |
| PHP | Server-side scripting language |
| MariaDB | Database backend |
| phpMyAdmin | Database administration |
| osTicket v1.18.4 | Help Desk ticketing platform |
| Google Chrome | Testing and administration |

## Project Objectives

The primary goal of this project was to gain hands-on experience deploying, configuring, and administering an enterprise help desk environment while simulating the responsibilities of a Tier 1 IT Support Technician.

Project objectives included:

- Deploy osTicket using XAMPP, Apache, PHP, and MariaDB.
- Configure departments, agents, and Role-Based Access Control (RBAC).
- Configure ticket settings, notifications, and administrative preferences.
- Process support tickets through the complete ticket lifecycle.
- Document common troubleshooting scenarios.
- Produce professional technical documentation suitable for an IT support portfolio.

  ## Installation & Deployment

The first phase of the project involved deploying osTicket in a local Windows environment using XAMPP. This included configuring the web server, creating the database, completing the installation wizard, and securing the application after deployment.

### 1. Install XAMPP

XAMPP was installed to provide the Apache web server, PHP runtime, and MariaDB database required to host osTicket locally. After installation, the Apache and MySQL services were started and verified through the XAMPP Control Panel.

![XAMPP Control Panel](assets/images/Screenshot%202026-07-02%20224251.png)



### 2. Deploy the osTicket Files

The osTicket installation files were extracted into the XAMPP `htdocs` directory, making the application accessible through the local Apache web server.

The installer prerequisites were verified to ensure the required PHP extensions and server components were enabled before continuing with the installation.

![osTicket Installer Prerequisites Check](assets/images/Screenshot%202026-07-03%20000236.png)



### 3. Configure the Database

A dedicated MariaDB database was created using phpMyAdmin. A database user was also created and assigned the appropriate privileges required by osTicket.

These credentials were later used during the installation wizard to establish the database connection.

![phpMyAdmin Database Creation](assets/images/Screenshot%202026-07-05%20110505.png)


![Database User Configuration](assets/images/Screenshot%202026-07-05%20115837.png)
> - phpMyAdmin Database Creation
> - Database User Configuration

---

### 4. Complete the Installation

The osTicket installation wizard was completed by configuring:

- Help Desk Name
- Default Administrator Account
- Administrator Email
- Database Connection
- Database Credentials

After installation, the application successfully connected to the MariaDB database and generated the initial help desk environment.

![osTicket Installation Complete](assets/images/Screenshot%202026-07-04%20211009.png)


### 5. Secure the Installation

After confirming a successful installation, the default setup directory was removed and the configuration file permissions were updated to prevent unauthorized modifications.

These post-installation security steps are recommended as part of the official osTicket deployment process.

![Installation Complete / Security Reminder](assets/images/Screenshot%202026-07-05%20105837.png)

## System Configuration

After completing the installation, the osTicket environment was configured to simulate an enterprise IT help desk. Administrative settings were customized to establish departments, configure agent accounts, define access permissions, and manage ticket handling. These tasks demonstrate the responsibilities commonly performed by Help Desk and Systems Administrators when deploying and maintaining a ticketing platform.


### Department Configuration

Departments were created to organize support responsibilities and route incoming requests to the appropriate teams. Creating separate departments improves ticket organization, accountability, and workflow management.

The following departments were configured within the help desk environment:

- Help Desk
- Sales & Billing
- Network Operations
- Cyber Security
- Cloud Services
- Human Resources
- System Administration

![Agent Account Configuration](assets/images/Screenshot%202026-07-05%20111919.png)

*Figure 1. Department structure configured within the osTicket administrative portal.*

---

### Agent Configuration

Support agents were configured with department assignments, access permissions, and team memberships. Agent accounts were created to simulate multiple IT support technicians working within a structured help desk environment.

Configuration included:

- Creating agent accounts
- Assigning primary departments
- Configuring extended department access
- Assigning security roles
- Assigning team memberships
- Configuring agent permissions

![Agent Account Configuration](assets/images/Screenshot%202026-07-05%20115819.png)

*Figure 2. Creating a new support agent account.*

![Configuring Department Access and Security Roles](assets/images/Screenshot%202026-07-05%20115826.png)

*Figure 3. Configuring department access and security roles.*

![Configuring Department Access and Security Roles](assets/images/Screenshot%202026-07-05%20120916.png)

*Figure 4. Assigning permissions to support agents.*

![Assigning Permissions to Support Agents](assets/images/Screenshot%202026-07-05%20115837.png)

*Figure 5. Assigning agents to support teams.*

![Assigning Agents to Support Teams](assets/images/Screenshot%202026-07-05%20115850.png)

### Roles and Permissions (RBAC)

Role-Based Access Control (RBAC) was implemented to define the permissions available to support personnel. Roles were configured to ensure agents had access only to the resources required for their responsibilities, following the principle of least privilege.

Permission sets were reviewed across several administrative areas, including:

- Ticket Management
- Task Management
- Knowledge Base Management

These configurations demonstrate how administrative access can be delegated while maintaining security and operational control.

![Role Configuration](assets/screenshots/role-configuration.png)

*Figure 6. Creating and managing support roles.*

![Ticket Permissions](assets/screenshots/ticket-permissions.png)

*Figure 7. Ticket permission configuration.*

![Task Permissions](assets/screenshots/task-permissions.png)

*Figure 8. Task permission configuration.*

![Knowledgebase Permissions](assets/screenshots/knowledgebase-permissions.png)

*Figure 9. Knowledge Base permission configuration.*

---

### Ticket Settings

Ticket settings were configured to establish consistent ticket handling procedures across the help desk environment. Default ticket behavior, SLA assignments, priorities, and workflow settings were reviewed to support standardized incident management.

Configuration included:

- Default ticket status
- Default priority
- Default SLA plan
- Ticket numbering format
- Help topic settings
- Ticket queue configuration
- Ticket locking behavior
- Attachment settings

![Ticket Settings](assets/screenshots/ticket-settings.png)

*Figure 10. Default ticket settings and workflow configuration.*

---

### Notifications and Autoresponder

Notification settings were configured to control how users and support staff are informed throughout the ticket lifecycle. Automatic notifications help ensure users receive updates while keeping technicians informed of new assignments and ticket activity.

Configuration included:

- Ticket autoresponder settings
- New ticket notifications
- New message alerts
- Internal activity alerts
- Ticket assignment notifications
- Ticket transfer notifications

![Autoresponder](assets/screenshots/autoresponder.png)

*Figure 11. Autoresponder configuration.*

![Alerts and Notices](assets/screenshots/alerts-notices.png)

*Figure 12. Ticket notification and alert configuration.*

---

### Configuration Validation

After completing the administrative configuration, each section was reviewed to verify that departments, agents, roles, permissions, and ticket settings had been successfully applied.

The environment was validated prior to creating and processing support tickets to ensure the help desk was fully operational and ready for testing.

## Ticket Lifecycle & Incident Management

After completing the system configuration, support tickets were created and managed to validate the help desk workflow within the osTicket environment. The following screenshots illustrate the process of creating, reviewing, assigning, and updating support requests.

---

### Creating a Support Ticket

A support request was submitted through the osTicket customer portal. During ticket creation, the requester provided contact information, selected a Help Topic, and entered a description of the issue before submitting the request.

![Open New Ticket](assets/screenshots/open-new-ticket.png)

*Figure 13. Customer portal used to submit a new support request.*

After submission, the system generated a confirmation page containing the newly assigned ticket number, indicating that the request had been successfully received.

![Ticket Created](assets/screenshots/ticket-created.png)

*Figure 14. Confirmation page displayed after successfully creating a support ticket.*

---

### Reviewing the Ticket Queue

Once submitted, the ticket appeared in the help desk queue where support staff could review incoming requests and monitor ticket activity.

The queue provides technicians with a centralized view of active tickets and their current status.

![Open Ticket Queue](assets/screenshots/open-ticket-queue.png)

*Figure 15. Open ticket queue displaying active support requests.*

A separate queue was also used to display tickets assigned to the currently logged-in technician.

![Assigned Tickets](assets/screenshots/assigned-tickets.png)

*Figure 16. Tickets assigned to the current support agent.*

---

### Reviewing Ticket Details

Individual tickets were opened to review the information submitted by the user. The ticket view displays important details including the requester, department, priority, assignment information, and the conversation history associated with the incident.

The example shown documents a support request involving shared drive access.

![Ticket Details](assets/screenshots/shared-drive-ticket.png)

*Figure 17. Reviewing the details of a support ticket within the agent portal.*

---

### Updating the Ticket

After reviewing the request, an update was entered into the ticket documenting the resolution. Recording updates within the ticket provides a history of actions taken and keeps the requester informed throughout the support process.

![Ticket Response](assets/screenshots/ticket-response.png)

*Figure 18. Posting an update to document the resolution of the support request.*

---

### Ticket Workflow Summary

The screenshots above demonstrate the core workflow performed within the osTicket environment:

1. A user submits a support request through the customer portal.
2. The ticket is successfully created and assigned a ticket number.
3. The request appears in the help desk queue.
4. A support technician reviews the ticket details.
5. An update is posted to document the actions taken to resolve the issue.

This workflow provided hands-on experience navigating the osTicket interface, managing support requests, documenting ticket updates, and following a structured help desk process.

## Troubleshooting

During the deployment and configuration of the osTicket environment, several issues were encountered and reviewed. Troubleshooting these events provided additional experience interpreting system messages, reviewing application logs, and understanding common configuration issues encountered during a help desk deployment.

---

### Mailer Error

During testing, the system generated mailer errors when attempting to send email notifications. This occurred because an SMTP mail server had not yet been configured for the lab environment.

Although email delivery was unavailable during testing, the application continued to function normally for ticket creation and management.

![Mailer Error](assets/screenshots/mailer-error.png)

*Figure 19. Mailer error generated while attempting to send email notifications without an SMTP server.*

---

### Invalid CSRF Token

During testing, an "Invalid CSRF Token" message was encountered. CSRF (Cross-Site Request Forgery) tokens are security mechanisms used to verify that requests originate from authenticated user sessions.

Refreshing the session and repeating the action resolved the issue.

![Invalid CSRF Token](assets/screenshots/csrf-token.png)

*Figure 20. CSRF validation message encountered during testing.*

---

### System Logs

The osTicket system logs were reviewed to identify application events and error messages generated during testing. Reviewing logs is an important troubleshooting technique that assists administrators in diagnosing configuration issues and monitoring system activity.

![System Logs](assets/screenshots/system-logs.png)

*Figure 21. Reviewing system logs within the osTicket administration portal.*

---

### Troubleshooting Summary

Reviewing application errors and system logs reinforced the importance of verifying system configuration, understanding security protections, and using administrative logging tools to diagnose issues. These experiences provided practical exposure to troubleshooting tasks commonly performed by Help Desk and Systems Administrators.

## Lessons Learned

This project provided practical experience deploying, configuring, and administering a help desk platform within a Windows environment. Beyond installing the application, the lab demonstrated the importance of planning the organizational structure of a help desk, assigning appropriate permissions, and documenting support activities throughout the ticket lifecycle.

Key takeaways from this project include:

- Deploying a PHP-based web application using Apache, MariaDB, and XAMPP.
- Configuring departments, agent accounts, and Role-Based Access Control (RBAC).
- Understanding how ticket queues, assignments, and user communication support daily help desk operations.
- Reviewing application logs and system messages to troubleshoot common configuration issues.
- Recognizing the importance of clear documentation for maintaining consistency and supporting future troubleshooting efforts.

Completing this lab strengthened my understanding of how enterprise help desk platforms are deployed, administered, and used to support end users in a structured IT environment.

## Skills Demonstrated

This project provided hands-on experience with the following technologies and IT support concepts:

### Systems Administration

- Windows 11
- XAMPP
- Apache
- PHP
- MariaDB
- phpMyAdmin

### Help Desk Administration

- osTicket Administration
- Department and Agent Configuration
- Ticket Queue Management
- Ticket Lifecycle Management
- Notification and Autoresponder Configuration

### Identity & Access Management

- Role-Based Access Control (RBAC)
- Permission Management
- Department and Team Assignment
- Principle of Least Privilege

### Troubleshooting & Documentation

- System Log Analysis
- Configuration Validation
- Basic Application Troubleshooting
- Technical Documentation
- Incident Documentation
- Problem Solving
