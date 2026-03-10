# Claims App

Custom Frappe app built as an HR-focused portfolio project.

## Overview

This app demonstrates practical Frappe development beyond basic UI configuration. It combines custom DocTypes, workflows, client scripts, and server-side validation for HR-style business processes.

## Modules

### Employee Claim

- custom `Employee Claim` DocType
- approval workflow: `Draft` -> `Pending Approval` -> `Approved` or `Rejected`
- client script to show or hide `Receipt` based on `Claim Type`
- server validation to require receipts for medical and travel claims
- amount validation to prevent invalid submissions

### Leave Request

- custom `Leave Request` DocType
- approval workflow for leave submission and review
- client script to auto-calculate total leave days from date range
- server validation to prevent invalid date ranges and non-positive day counts

### Attendance Adjustment

- custom `Attendance Adjustment` DocType
- approval workflow for attendance correction requests
- client script to validate requested check-in and check-out times
- server validation to require a reason and prevent invalid time ranges

### Recruitment Pipeline

- custom `Recruitment Pipeline` DocType
- workflow to move candidates from application to hiring or rejection
- client script to update overall status from recruitment stage
- server validation for required candidate details and basic email format

## Stack

- Frappe Framework
- Python
- JavaScript
- MariaDB
- Redis

## Included Records

- `Module Def`: `Claims Management`
- `DocType`: `Employee Claim`
- `DocType`: `Leave Request`
- `DocType`: `Attendance Adjustment`
- `DocType`: `Recruitment Pipeline`
- `Workflow`: employee claim approval flow
- `Workflow`: leave request approval flow
- `Workflow`: attendance adjustment approval flow
- `Workflow`: recruitment pipeline stage flow
- `Client Script`: employee claim receipt rule
- `Client Script`: leave request day calculation
- `Client Script`: attendance time validation
- `Client Script`: recruitment status update
- `Server Script`: employee claim validation
- `Server Script`: leave request validation
- `Server Script`: attendance adjustment validation
- `Server Script`: recruitment validation

## Local Setup

```bash
cd ~/frappe/my-bench
source ~/.local/bin/env
bench --site dev.localhost install-app claims_app
bench --site dev.localhost migrate
bench start
```

Open `http://dev.localhost:8000`.

## Export Fixtures

```bash
cd ~/frappe/my-bench
source ~/.local/bin/env
bench --site dev.localhost export-fixtures --app claims_app
```

## GitHub Value

This project shows:

- low-code setup with DocTypes and workflows
- custom frontend behavior with Frappe client scripts
- backend business rules with server-side validation
- HR-oriented product thinking relevant to claims, leave, attendance, and hiring flows
