## Process Flow

### Campaign Workflow Management System

---

## 1. Overview

This document describes the end-to-end process flow of the Campaign Workflow Management System, covering campaign creation, approval workflow, execution, and closure.

The objective of this workflow is to ensure a structured, transparent, and auditable campaign approval lifecycle.

---

## 2. High-Level Process Flow

The campaign lifecycle consists of the following stages:

1. Campaign Creation
2. Manager Review
3. Finance Approval
4. Final Approval
5. Campaign Execution
6. Campaign Closure

---

## 3. Detailed Process Steps

### Step 1: Campaign Creation

* Marketing Executive logs into the system
* Creates a new campaign
* Fills required details (Name, Budget, Timeline, Description)
* Saves as Draft or Submits for approval

**Status:** Draft / Pending Manager Approval

---

### Step 2: Manager Review

* Manager receives notification
* Reviews campaign details
* Approves or Rejects

If Rejected:

* Status updated to “Rejected by Manager”
* Comments mandatory
* Returned to Marketing Executive

If Approved:

* Routed to Finance

**Status:** Pending Finance Approval

---

### Step 3: Finance Approval

* Finance validates budget
* Reviews financial feasibility
* Approves or Rejects

If Rejected:

* Status updated to “Rejected by Finance”
* Returned to Marketing Executive

If Approved:

* Moves to Final Approval

---

### Step 4: Final Approval

* Final authority validates campaign compliance
* Approves campaign for execution

**Status:** Approved

---

### Step 5: Campaign Execution

* Marketing team executes campaign
* Progress tracked in dashboard

**Status:** In Execution

---

### Step 6: Campaign Closure

* Campaign marked as completed
* Final status updated
* All actions recorded in audit trail

**Status:** Closed

---

## 4. Workflow Diagram

You should include a diagram image inside the repository.

Example markdown reference:

```
![Campaign Process Flow](diagrams/process_flow.png)
```

---

## 5. Decision Points in Workflow

The process includes the following decision gateways:

* Manager Approval Decision
* Finance Budget Validation Decision
* Final Approval Decision

Each rejection loops back to the Marketing Executive for modification and resubmission.

---

## 6. Status Transition Flow

Draft
→ Pending Manager Approval
→ Pending Finance Approval
→ Approved
→ In Execution
→ Closed

Rejection at any stage returns the campaign to Draft status after revision.

---

## 7. Process Controls

* Mandatory comments on rejection
* Audit trail logging for every action
* Role-based restrictions on status updates
* Automated notifications at each transition


