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
- `Workflow`: employee claim approval flow
- `Workflow`: leave request approval flow
- `Client Script`: employee claim receipt rule
- `Client Script`: leave request day calculation
- `Server Script`: employee claim validation
- `Server Script`: leave request validation

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
- HR-oriented product thinking relevant to leave and claim management
