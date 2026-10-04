# Lab_03_Sujan_S_Halannanavar_PES1UG24CS477



# Lab 3 — Component Modelling & Architectural Selection

## Problem Statement #46
### Remote Team Time-Tracking & Project Approver System

**Course:** Software Engineering (CS301)  
**Lab:** Lab 3 — Component Modelling & Architectural Selection  
**Problem Statement:** #46  
**Architecture:** 3-Tier Layered Architecture with a Client-Server deployment model

---

## 1. Objective

The objective of this lab is to model the architecture of the Remote Team Time-Tracking & Project Approver System using UML component modelling and to justify the selected architectural style.

---

## 2. Selected Architecture

The system uses a **3-Tier Layered Architecture with a Client-Server deployment model**.

The architecture is divided into three main layers:

### Client / Presentation Layer

- Developer Web Client Component
- Manager Dashboard Component

### Application / Business Logic Layer

- Timesheet Manager Component
- Validation Engine Component
- Jira Integration Component
- Budget Analytics Component

### Data / Persistence Layer

- Timesheet & Budget Database Component

---

## 3. Main Actors and External System

### Remote Developer

The Remote Developer logs time against project tasks or Jira tickets and submits completed timesheets.

### Engineering Manager

The Engineering Manager reviews submitted timesheets, approves or rejects them, and views project budget burn-rate information.

### Jira Project Management System

Jira provides project tasks, tickets, and relevant worklog information to the system through the Jira Integration Component.

---

## 4. Main Components

| Component | Layer | Main Responsibility |
|---|---|---|
| Developer Web Client Component | Client / Presentation | Time logging and timesheet submission |
| Manager Dashboard Component | Client / Presentation | Timesheet review, approval, rejection, and budget monitoring |
| Timesheet Manager Component | Application / Business Logic | Timesheet workflow and approval management |
| Validation Engine Component | Application / Business Logic | Timesheet validation and 24-hour daily limit |
| Jira Integration Component | Application / Business Logic | Jira task and worklog integration |
| Budget Analytics Component | Application / Business Logic | Project budget burn-rate calculations |
| Timesheet & Budget Database Component | Data / Persistence | Storage of timesheets, approvals, audit records, and budget information |

---

## 5. Main Interfaces

The component diagram contains the following major interfaces:

1. **Timesheet REST API**
2. **Jira Sync Interface**
3. **Validation Interface**
4. **Analytics Interface**
5. **Database Persistence Interface**

These interfaces show the communication and dependencies between the system components.

---

## 6. Important System Requirements Represented

The architecture supports the following key requirements:

- Developers can log time against project tasks or Jira tickets.
- Developers can submit completed timesheets.
- Timesheets are validated before submission.
- The system prevents more than 24 hours from being recorded on a single calendar day.
- Engineering Managers can review submitted timesheets.
- Engineering Managers can approve or reject timesheets.
- Engineering Managers can view project budget burn-rate information.
- Only authenticated Engineering Managers can approve or reject timesheets.
- Timesheet status and budget burn-rate information should be updated within 500 ms.

---

## 7. Files Included

- `Problem_46_Component_Diagram.pdf` — UML Component Diagram
- `Problem_46_Architecture_Justification.pdf` — Architectural Justification
- `Problem_46_Component_Diagram.drawio` — Editable draw.io source file (if included)

---

## 8. Conclusion

The selected 3-Tier Layered Architecture with a Client-Server deployment model provides a clear separation between presentation, business logic, and data management. It supports centralized timesheet processing, validation, approval workflows, Jira integration, security, and project budget monitoring for the Remote Team Time-Tracking & Project Approver System.
