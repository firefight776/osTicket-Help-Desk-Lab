# osTicket Help Desk Lab

## Project Overview

This project documents the deployment and configuration of an osTicket help desk environment on Windows using XAMPP, Apache, PHP, and MariaDB.

The lab was designed to simulate the daily operations of an internal IT department or managed service provider. It includes role-based access control, departments, agent accounts, ticket routing, SLA configuration, notification settings, and realistic Tier 1 support incidents.

The completed environment was used to create, assign, investigate, update, resolve, and close support tickets while documenting the troubleshooting process and final outcomes.

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
- Configure departments, roles, and agent permissions using Role-Based Access Control (RBAC).
- Create a structured help desk environment to simulate an internal corporate IT support team.
- Configure system settings, ticket routing, and default department assignments.
- Create and manage support tickets throughout their lifecycle.
- Practice ticket assignment, escalation, and resolution workflows.
- Document troubleshooting procedures for common IT support incidents.
- Develop experience with ticket documentation, customer communication, and incident management.
- Build a professional IT Support portfolio project demonstrating practical help desk administration skills.

  ## Installation & Deployment

The first phase of the project involved deploying osTicket in a local Windows environment using XAMPP. This included configuring the web server, creating the database, completing the installation wizard, and securing the application after deployment.

### 1. Install XAMPP

XAMPP was installed to provide the Apache web server, PHP runtime, and MariaDB database required to host osTicket locally. After installation, the Apache and MySQL services were started and verified through the XAMPP Control Panel.

> **Screenshot:** XAMPP Control Panel

---

### 2. Deploy the osTicket Files

The osTicket installation files were extracted into the XAMPP `htdocs` directory, making the application accessible through the local Apache web server.

The installer prerequisites were verified to ensure the required PHP extensions and server components were enabled before continuing with the installation.

> **Screenshot:** osTicket Installer – Prerequisites Check

---

### 3. Configure the Database

A dedicated MariaDB database was created using phpMyAdmin. A database user was also created and assigned the appropriate privileges required by osTicket.

These credentials were later used during the installation wizard to establish the database connection.

> **Screenshots:**
>
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

> **Screenshot:** Installation Complete

---

### 5. Secure the Installation

After confirming a successful installation, the default setup directory was removed and the configuration file permissions were updated to prevent unauthorized modifications.

These post-installation security steps are recommended as part of the official osTicket deployment process.

> **Screenshot:** Installation Complete / Security Reminder

## System Configuration

After completing the installation, the osTicket environment was configured through the administrative control panel. The initial configuration established the organizational structure of the help desk by defining system settings, departments, roles, and access permissions. These administrative tasks mirror the responsibilities commonly performed by Help Desk and Systems Administrators when deploying a new ticketing platform.

---

### System Settings

The system settings were reviewed and updated to establish the core configuration of the help desk environment. This included verifying the application's general settings and confirming that configuration changes were successfully applied.

![System Settings](assets/screenshots/system-settings.png)

*Figure 1. General system configuration within the osTicket Administration Panel.*

---

### Agent Settings

Agent settings were reviewed to configure how support staff interact with the help desk environment. These settings determine how agents authenticate, manage tickets, and perform administrative tasks within the system.

![Agent Settings](assets/screenshots/agent-settings.png)

*Figure 2. Agent configuration options used to manage support personnel.*

---

### Department Configuration

Departments were created to organize support responsibilities and provide a structured workflow for routing and managing incoming requests. Organizing tickets by department helps ensure requests are directed to the appropriate support team.

![Create Department](assets/screenshots/create-department.png)

*Figure 3. Creating a department within the administrative portal.*

![Department List](assets/screenshots/department-list.png)

*Figure 4. Configured departments available within the help desk environment.*

---

### Roles and Permissions (RBAC)

Role-Based Access Control (RBAC) was configured to define the permissions available to support agents. Permission sets were reviewed across multiple administrative areas to demonstrate how access can be limited according to job responsibilities while following the principle of least privilege.

Administrative permissions were reviewed for:

- Ticket Management
- Task Management
- Knowledge Base Management

![Role Configuration](assets/screenshots/role-configuration.png)

*Figure 5. Creating and managing administrative roles.*

![Ticket Permissions](assets/screenshots/ticket-permissions.png)

*Figure 6. Ticket permission configuration.*

![Task Permissions](assets/screenshots/task-permissions.png)

*Figure 7. Task permission configuration.*

![Knowledgebase Permissions](assets/screenshots/knowledgebase-permissions.png)

*Figure 8. Knowledge Base permission configuration.*

---

### Configuration Validation

After completing the administrative configuration, the environment was reviewed to verify that changes were successfully applied.

During role creation, a validation error was encountered and documented as part of the troubleshooting process. Capturing and resolving configuration issues is an important aspect of systems administration and help desk operations.

![Settings Saved](assets/screenshots/settings-saved.png)

*Figure 9. Successful confirmation after updating administrative settings.*

![Role Validation Error](assets/screenshots/role-validation-error.png)

*Figure 10. Validation error encountered during role configuration.*
