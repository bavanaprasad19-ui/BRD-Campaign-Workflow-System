## Functional Requirements

### Campaign Workflow Management System

---

## 1. Introduction

This document defines the detailed functional requirements of the Campaign Workflow Management System. These requirements describe system behavior, user interactions, and workflow rules necessary to fulfill the business objectives defined in the BRD.

---

## 2. User Roles

The system shall support the following roles:

* Marketing Executive
* Marketing Manager
* Finance Officer
* Admin

Each role shall have role-based access permissions.

---

## 3. Functional Requirements

### 3.1 User Authentication & Access Control

| FR ID | Requirement Description                                               | Priority |
| ----- | --------------------------------------------------------------------- | -------- |
| FR-01 | The system shall allow users to log in using valid credentials.       | High     |
| FR-02 | The system shall restrict access based on user role.                  | High     |
| FR-03 | The system shall allow Admin to create, modify, and deactivate users. | High     |
| FR-04 | The system shall log out users after session timeout.                 | Medium   |

---

### 3.2 Campaign Creation

| FR ID | Requirement Description                                                                                      | Priority |
| ----- | ------------------------------------------------------------------------------------------------------------ | -------- |
| FR-05 | The system shall allow Marketing Executive to create a new campaign.                                         | High     |
| FR-06 | The campaign form shall capture mandatory fields (Campaign Name, Description, Start Date, End Date, Budget). | High     |
| FR-07 | The system shall validate mandatory fields before submission.                                                | High     |
| FR-08 | The system shall allow users to save campaign as Draft.                                                      | Medium   |

---

### 3.3 Campaign Submission & Approval Workflow

| FR ID | Requirement Description                                                    | Priority |
| ----- | -------------------------------------------------------------------------- | -------- |
| FR-09 | The system shall allow campaign submission for approval.                   | High     |
| FR-10 | Upon submission, the system shall route the campaign to Marketing Manager. | High     |
| FR-11 | Manager shall have options to Approve or Reject the campaign.              | High     |
| FR-12 | Rejection shall require mandatory comments.                                | High     |
| FR-13 | If approved by Manager, the system shall route the campaign to Finance.    | High     |
| FR-14 | Finance shall approve or reject based on budget validation.                | High     |
| FR-15 | Final approval status shall update campaign lifecycle status.              | High     |

---

### 3.4 Notifications

| FR ID | Requirement Description                                          | Priority |
| ----- | ---------------------------------------------------------------- | -------- |
| FR-16 | The system shall send email notification upon submission.        | Medium   |
| FR-17 | The system shall notify users on approval/rejection.             | Medium   |
| FR-18 | The system shall notify stakeholders when campaign is finalized. | Medium   |

---

### 3.5 Dashboard & Tracking

| FR ID | Requirement Description                                                                    | Priority |
| ----- | ------------------------------------------------------------------------------------------ | -------- |
| FR-19 | The system shall provide a dashboard displaying campaign status.                           | High     |
| FR-20 | The dashboard shall display counts by status (Draft, Pending, Approved, Rejected, Closed). | High     |
| FR-21 | Users shall be able to filter campaigns by date and status.                                | Medium   |
| FR-22 | Users shall be able to search campaigns by name.                                           | Medium   |

---

### 3.6 Campaign Status Management

| FR ID | Requirement Description                              | Priority |
| ----- | ---------------------------------------------------- | -------- |
| FR-23 | Approved campaigns shall move to “Execution” status. | High     |
| FR-24 | Completed campaigns shall move to “Closed” status.   | High     |
| FR-25 | Only authorized roles shall update campaign status.  | High     |

---

### 3.7 Audit Trail

| FR ID | Requirement Description                                        | Priority |
| ----- | -------------------------------------------------------------- | -------- |
| FR-26 | The system shall maintain audit logs of all actions.           | High     |
| FR-27 | Audit logs shall record user, timestamp, and action performed. | High     |
| FR-28 | Admin shall have access to view audit logs.                    | Medium   |

---

## 4. Functional Workflow Summary

1. User logs into system
2. Marketing Executive creates campaign
3. Campaign submitted to Manager
4. Manager approves/rejects
5. If approved → routed to Finance
6. Finance approves/rejects
7. Status updated accordingly
8. Campaign executed and closed
9. All actions recorded in audit log

---

## 5. Traceability Note

Each functional requirement (FR) is traceable to corresponding Business Requirement (BR) defined in the BRD document. Mapping is maintained in the RTM document.
