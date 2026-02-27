## Use Case Specification

### Campaign Workflow Management System

---

## 1. Introduction

This document provides detailed use case specifications for key system functionalities of the Campaign Workflow Management System.

Each use case defines actors, preconditions, main flow, alternate flows, and postconditions to ensure clarity and completeness.

---

# Use Case 1: Create Campaign

## Use Case ID

UC-01

## Use Case Name

Create Campaign

## Primary Actor

Marketing Executive

## Stakeholders

* Marketing Manager
* Finance Team

## Preconditions

* User must be logged into the system
* User must have Marketing Executive role

## Trigger

User selects “Create Campaign” option

## Main Flow

1. User clicks “Create Campaign”
2. System displays campaign creation form
3. User enters required details
4. User clicks “Save” or “Submit”
5. System validates mandatory fields
6. If valid, campaign is saved

## Alternate Flow

**A1: Missing Mandatory Fields**

* System displays validation error
* User corrects input

**A2: Save as Draft**

* Campaign saved with Draft status
* No approval workflow triggered

## Postconditions

* Campaign created successfully
* Status set to Draft or Pending Manager Approval

---

# Use Case 2: Manager Approval

## Use Case ID

UC-02

## Use Case Name

Review and Approve Campaign

## Primary Actor

Marketing Manager

## Preconditions

* Campaign must be submitted
* Status must be “Pending Manager Approval”

## Trigger

Manager opens pending campaign

## Main Flow

1. Manager reviews campaign details
2. Manager selects Approve
3. System updates status
4. System routes campaign to Finance
5. Notification sent to Finance

## Alternate Flow

**A1: Reject Campaign**

1. Manager selects Reject
2. System requires rejection comments
3. Status updated to “Rejected by Manager”
4. Notification sent to Marketing Executive

## Postconditions

* Campaign moves to Finance stage
  OR
* Campaign returned to Marketing Executive

---

# Use Case 3: Finance Validation

## Use Case ID

UC-03

## Use Case Name

Budget Approval

## Primary Actor

Finance Officer

## Preconditions

* Campaign approved by Manager
* Status = Pending Finance Approval

## Trigger

Finance reviews campaign

## Main Flow

1. Finance validates budget details
2. Finance selects Approve
3. Status updated to Approved
4. Campaign moves to Execution stage

## Alternate Flow

**A1: Reject Due to Budget Issue**

1. Finance selects Reject
2. Comments mandatory
3. Status updated to “Rejected by Finance”
4. Notification sent to Marketing Executive

## Postconditions

* Campaign approved for execution
  OR
* Campaign returned for modification

---

# Use Case 4: View Dashboard

## Use Case ID

UC-04

## Use Case Name

View Campaign Dashboard

## Primary Actor

All Authorized Users

## Preconditions

* User logged in

## Trigger

User selects Dashboard

## Main Flow

1. System displays campaigns grouped by status
2. User filters by date/status
3. User views campaign details

## Alternate Flow

**A1: No Records Found**

* System displays “No Campaigns Available”

## Postconditions

* User obtains real-time campaign insights

---

# Use Case 5: Close Campaign

## Use Case ID

UC-05

## Use Case Name

Close Campaign

## Primary Actor

Marketing Executive / Authorized User

## Preconditions

* Campaign status = In Execution

## Trigger

User selects “Mark as Closed”

## Main Flow

1. User confirms closure
2. System updates status to Closed
3. Audit log entry created

## Postconditions

* Campaign lifecycle completed
* Dashboard updated

---

# 7. Business Rules Reference

* Rejection requires mandatory comments
* Only authorized roles can approve
* Status transitions must follow defined workflow
* All actions must be recorded in audit trail
