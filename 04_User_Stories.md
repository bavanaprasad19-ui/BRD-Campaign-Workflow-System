## User Stories

### Campaign Workflow Management System

---

## 1. Introduction

This document defines user stories for the Campaign Workflow Management System.
Each story follows Agile format and includes acceptance criteria to ensure clarity and testability.

---

## 2. Epic 1: User Authentication & Access Control

### US-01: User Login

**As a** system user
**I want to** log in using valid credentials
**So that** I can securely access the system

**Acceptance Criteria:**

* User must enter valid username and password
* System must validate credentials
* Invalid login attempts display error message
* Session expires after inactivity

---

### US-02: Role-Based Access

**As an** Admin
**I want to** assign roles to users
**So that** access is restricted based on responsibility

**Acceptance Criteria:**

* Admin can create, edit, deactivate users
* Users can only access permitted modules
* Unauthorized access attempts are restricted

---

## 3. Epic 2: Campaign Creation

### US-03: Create Campaign

**As a** Marketing Executive
**I want to** create a new campaign
**So that** I can initiate the approval workflow

**Acceptance Criteria:**

* Campaign form captures mandatory fields
* Mandatory fields must be validated
* User can save campaign as Draft
* Draft campaigns can be edited

---

### US-04: Submit Campaign

**As a** Marketing Executive
**I want to** submit campaign for approval
**So that** it can move to the review stage

**Acceptance Criteria:**

* Only completed campaigns can be submitted
* Submission triggers notification to Manager
* Campaign status changes to “Pending Manager Approval”

---

## 4. Epic 3: Approval Workflow

### US-05: Manager Review

**As a** Marketing Manager
**I want to** review campaign details
**So that** I can approve or reject it

**Acceptance Criteria:**

* Manager can view complete campaign details
* Manager can approve or reject
* Rejection requires mandatory comments
* Status updates accordingly

---

### US-06: Finance Validation

**As a** Finance Officer
**I want to** validate campaign budget
**So that** financial compliance is maintained

**Acceptance Criteria:**

* Finance can approve or reject after Manager approval
* Budget details must be visible
* Rejection requires reason
* Status updates accordingly

---

## 5. Epic 4: Notifications

### US-07: Workflow Notifications

**As a** system user
**I want to** receive email notifications
**So that** I stay informed of campaign status changes

**Acceptance Criteria:**

* Notification sent on submission
* Notification sent on approval/rejection
* Notification includes campaign details and status

---

## 6. Epic 5: Dashboard & Tracking

### US-08: View Dashboard

**As a** user
**I want to** view campaign dashboard
**So that** I can track campaign progress

**Acceptance Criteria:**

* Dashboard displays campaigns by status
* Users can filter by date and status
* Users can search by campaign name

---

### US-09: Update Campaign Status

**As a** authorized user
**I want to** update campaign status to Closed
**So that** campaign lifecycle is completed

**Acceptance Criteria:**

* Only authorized roles can update status
* Status changes are logged in audit trail

---

## 7. Epic 6: Audit Trail

### US-10: Maintain Audit Log

**As an** Admin
**I want to** view activity logs
**So that** I can track all system actions

**Acceptance Criteria:**

* System logs user, timestamp, and action
* Logs cannot be modified
* Admin can filter logs by date

---

## 8. Story Prioritization Approach

Stories are prioritized based on:

* Business criticality
* Workflow dependency
* Impact on campaign lifecycle
* Risk level

High-priority stories include login, campaign submission, and approval workflow.
