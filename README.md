# Claims App

Custom Frappe app for an employee claims workflow portfolio project.

## Features

- Custom `Employee Claim` DocType
- Claim approval workflow
- Client-side receipt visibility rules
- Server-side validation for receipt and amount
- Custom module: `Claims Management`

## Stack

- Frappe Framework
- Python
- JavaScript
- MariaDB

## Included Records

- `Module Def`: `Claims Management`
- `DocType`: `Employee Claim`
- `Workflow`: employee claim approval flow
- `Client Script`: receipt visibility rule
- `Server Script`: claim validation

## Local Setup

```bash
cd ~/frappe/my-bench
bench --site dev.localhost install-app claims_app
bench --site dev.localhost migrate
bench start
```

## Export Fixtures

```bash
cd ~/frappe/my-bench
bench --site dev.localhost export-fixtures --app claims_app
```

## Portfolio Value

This project demonstrates both sides of Frappe development:

- low-code setup with DocTypes and workflow
- code-based customization with JavaScript and backend validation
