# Test Plan: SauceDemo E-Commerce Manual Testing

---

## 1. Document Control & Overview

| Project Name                     | SauceDemo E-Commerce Manual Testing Portfolio              |
| :------------------------------- | :--------------------------------------------------------- |
| **Application Under Test (AUT)** | [SauceDemo (Swag Labs)](https://www.saucedemo.com/)        |
| **Target Audience**              | QA Hiring Managers, Senior Engineers, Technical Recruiters |
| **Author**                       | QA Engineer (Portfolio Project)                            |
| **Version**                      | 1.0.0                                                      |
| **Date**                         | October 2026                                               |

---

## 2. Executive Summary & Objectives

The primary objective of this project is to conduct end-to-end manual software testing on the **SauceDemo** web application to ensure its functional integrity, user interface usability, input validation robustness, security access control, and cross-browser consistency.

### Primary Objectives:

- Ensure seamless authentication workflows for all user personas provided by SauceDemo.
- Validate inventory browsing, sorting algorithms (Alphabetical & Price-based), cart state management, and end-to-end multi-step checkout processes.
- Identify edge cases, boundary conditions, input validation limits, and session access flaws.
- Maintain standardized, production-ready QA artifacts suitable for enterprise testing teams.

---

## 3. Scope of Testing

### 3.1 In-Scope Features

- **User Authentication & Authorization**:
  - Valid user login (`standard_user`).
  - User restriction scenarios (`locked_out_user`).
  - Problematic account behavior (`problem_user`).
  - Latency performance user (`performance_glitch_user`).
  - Form validation on empty/missing credentials.
- **Product Catalog & Inventory**:
  - Item listing layout, details page navigation, image integrity.
  - Sorting functionality (A-Z, Z-A, Price Low-High, Price High-Low).
- **Shopping Cart Management**:
  - Adding/removing items from both inventory catalog and dedicated cart page.
  - Cart counter badge dynamic updating.
  - Session state persistence when navigating between pages.
- **Checkout Workflow (Step 1 & Step 2)**:
  - First Name, Last Name, Postal Code field validation.
  - Cart item price subtotal, 8% tax calculation, and grand total verification.
  - Order submission and order completion acknowledgment.
- **Navigation & App State**:
  - Burger sidebar menu navigation (`All Items`, `About`, `Logout`, `Reset App State`).
- **Security & Session Safeguards**:
  - Restricted direct URL access without active login session.
  - Post-logout browser back button handling.

### 3.2 Out-of-Scope

- Backend API microservices testing (focused purely on UI/UX Manual Testing).
- Automated regression scripts (Selenium/Playwright) - reserved for separate portfolio project.
- Database layer validation (SQL queries).
- Payment Gateway live card authorization (mock application uses dummy card details).

---

## 4. Test Strategy & Types of Testing

| Testing Type                      | Description                                                     | Focus Area                                         |
| :-------------------------------- | :-------------------------------------------------------------- | :------------------------------------------------- |
| **Functional Testing**            | Verifying feature execution against expected business rules     | Login, Cart additions, Checkout finish, Navigation |
| **Negative Testing**              | Testing with invalid inputs, missing fields, or locked accounts | Blank fields, wrong passwords, locked users        |
| **Boundary Value Analysis (BVA)** | Validating input limits on postal codes and form fields         | Postal code formats, long strings                  |
| **UI / Usability Testing**        | Checking alignment, font legibility, broken images, layout      | Inventory item graphics, catalog alignment         |
| **Security / Access Control**     | Preventing unauthorized route traversal via direct URL pasting  | `/inventory.html`, `/cart.html` direct entry       |
| **State Reset & Session**         | Verifying session resets and state preservation across actions  | Side menu `Reset App State`, `Logout`              |

---

## 5. Test Environment & Requirements

### Hardware & Software Configuration:

- **Operating System**: Windows 11 / macOS Sonoma
- **Supported Browsers**: Google Chrome (v122+), Mozilla Firefox (v123+), Microsoft Edge (v122+)
- **Resolution**: 1920x1080 (Desktop Full HD), 1366x768 (Standard Laptop)
- **Application URL**: `https://www.saucedemo.com/`

---

## 6. Entry and Exit Criteria

### 6.1 Entry Criteria

1. Application Under Test (`https://www.saucedemo.com/`) is publicly accessible without network downtime.
2. Test Environment and browser configurations are set up.
3. Test Scenarios and Test Cases have been documented, reviewed, and finalized.
4. Test Data suites (credentials, form inputs) are available.

### 6.2 Exit Criteria

1. 100% of planned test cases (39/39) have a final execution status.
2. All discovered defects are reported in `BugReport.xlsx` with reproducible steps and available supporting evidence.
3. Critical and High severity bugs have been documented and submitted for development review.
4. Test Execution Report and Test Summary Report are finalized and signed off by QA.

---

## 7. Defect Management & Severity Matrix

Defects discovered during manual execution are logged in `Bug-Reports/BugReport.xlsx` using the following severity guidelines:

- **Critical (P1/S1)**: Application crash, system unresponsiveness, security bypass allowing unauthorized access.
- **High (P2/S2)**: Core functional failure with no workaround (e.g., Unable to complete checkout, login button non-functional).
- **Medium (P3/S3)**: Secondary feature defect or visual anomaly with existing workaround (e.g., Broken product images for `problem_user`, sorting anomaly).
- **Low (P4/S4)**: Cosmetic flaw, minor alignment issue, typo in error message string.

---

## 8. Risks and Mitigation Strategies

| Identified Risk                                           | Risk Impact | Mitigation Strategy                                                                 |
| :-------------------------------------------------------- | :---------- | :---------------------------------------------------------------------------------- |
| Web app server downtime during testing                    | High        | Validate server availability before execution session; report host issues promptly. |
| Browser update introducing rendering layout changes       | Low         | Document exact browser version used during execution in defect reports.             |
| Third-party link (`Sauce Labs` external site) unreachable | Low         | Mark external site links as out-of-scope for core app testing.                      |

---

## 9. Deliverables & Sign-Off

Upon conclusion of testing, the following artifacts are committed to GitHub:

1. `TestPlan.md` (This document)
2. `TestScenarios.md`
3. `TestCases.xlsx` / `TestCases.csv`
4. `BugReport.xlsx` / `BugReport.csv`
5. `TestExecutionReport.xlsx` / `TestExecutionReport.csv`
6. `TestSummaryReport.md`
7. `TestData.md`

---

_Prepared by Senior QA Engineer for portfolio verification._
