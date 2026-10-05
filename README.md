# E-Commerce Website Manual Testing Portfolio Project

![QA Testing](https://img.shields.io/badge/QA-Manual%20Testing-blue.svg)
![Application](https://img.shields.io/badge/AUT-SauceDemo-orange.svg)
![Status](https://img.shields.io/badge/Status-Partial%20Execution%20Complete-brightgreen.svg)
![Test Cases](https://img.shields.io/badge/Test%20Cases-38%20Defined-success.svg)
![Executed](https://img.shields.io/badge/Executed-8%20Pass%20(100%25)-success.svg)

A professional, interview-ready manual testing portfolio project built for the **SauceDemo** web application ([https://www.saucedemo.com/](https://www.saucedemo.com/)).

This repository demonstrates industry-standard Quality Assurance (QA) practices, including IEEE-style Test Planning, Scenario Mapping, 38 detailed Test Cases (covering Functional, Negative, Boundary, UI/UX, and Security aspects), Defect Reporting, Execution Tracking, and **documented test results with screenshot evidence** for executed scenarios.

---

## 📌 Application Under Test (AUT)

* **Application Name**: SauceDemo (Swag Labs)
* **URL**: [https://www.saucedemo.com/](https://www.saucedemo.com/)
* **Description**: A simulated e-commerce web application featuring authentication, product catalog display, sorting algorithms, cart state management, multi-step checkout workflow, and side menu management.

---

## ✅ Test Execution Summary (Evidence-Based)

Manual testing was performed on **5 October 2026**. **8 of 38** planned test cases were executed; **all 8 passed**. Screenshot proof is stored in [`Screenshots/`](Screenshots/).

| Test ID | Feature verified | Result | Evidence file |
| :--- | :--- | :---: | :--- |
| `TC_LOG_001` | Valid login → Products (`inventory.html`) | Pass | `TC_LOG_001_Valid_Login.png` |
| `TC_LOG_002` | Locked-out user error message | Pass | `TC_LOG_002_Locked_User.png` |
| `TC_INV_001` | Inventory page layout and product listing | Pass | `TC_INV_001_Inventory_Page.png` |
| `TC_INV_002` | Product detail page (Sauce Labs Backpack) | Pass | `TC_INV_002_Product_Details.png` |
| `TC_CRT_002` | Multiple items in cart (badge count 3) | Pass | `TC_CRT_002_Multiple_Products_Cart.png` |
| `TC_CHK_001` | Checkout Step 1 — Your Information | Pass | `TC_CHK_001_Checkout_Step1.png` |
| `TC_CHK_009` | Order completion — thank-you page | Pass | `TC_CHK_009_Order_Success.png` |
| `TC_SEC_001` | Block direct `/inventory.html` without login | Pass | `TC_SEC_001_Direct_URL_Access.png` |

**Observed functionality (from screenshots only):**

- **Login**: Successful session reaches the product catalog; `locked_out_user` is rejected with *Sorry, this user has been locked out.*
- **Catalog**: Six products with prices and **Add to cart**; default sort **Name (A to Z)** visible on inventory.
- **Product detail**: Item page shows image, description, price, **Add to cart**, and **Back to products**.
- **Cart**: Three items added; cart icon shows **3**; added lines switch to **Remove** on the inventory page.
- **Checkout**: Step-one form (First Name, Last Name, Zip/Postal Code) with **Continue** / **Cancel**; order completes with *Thank you for your order!* on `checkout-complete.html`.
- **Security**: Unauthenticated direct inventory access redirects to login with *You can only access '/inventory.html' when you are logged in.*

Full metrics and sign-off details: [`Test-Summary/TestSummaryReport.md`](Test-Summary/TestSummaryReport.md). Row-level execution status: [`Test-Execution/TestExecutionReport.csv`](Test-Execution/TestExecutionReport.csv).

---

## 📁 Repository Folder Structure

```text
ecommerce-manual-testing-saucedemo/
│
├── README.md                           # Main Project Documentation & Setup Guide
├── Test-Plan/
│   └── TestPlan.md                     # Comprehensive Test Plan (IEEE standard format)
├── Test-Scenarios/
│   └── TestScenarios.md                # High-Level Scenarios mapped to Test Cases
├── Test-Cases/
│   ├── TestCases.xlsx                  # 38 Detailed Test Cases (Formatted Excel)
│   └── TestCases.csv                   # CSV version for easy GitHub viewing
├── Bug-Reports/
│   ├── BugReport.xlsx                  # Defect Logging Template with Sample Bugs
│   └── BugReport.csv                   # CSV version for easy GitHub viewing
├── Test-Execution/
│   ├── TestExecutionReport.xlsx        # Test Execution Tracking Matrix & Dashboard
│   └── TestExecutionReport.csv         # CSV version — 8 executed / 30 pending
├── Test-Summary/
│   └── TestSummaryReport.md            # Test Summary with execution metrics & evidence
├── Test-Data/
│   └── TestData.md                     # Comprehensive Test Data Specifications
└── Screenshots/
    ├── README.md                       # Screenshot naming guidelines
    ├── TC_LOG_001_Valid_Login.png
    ├── TC_LOG_002_Locked_User.png
    ├── TC_INV_001_Inventory_Page.png
    ├── TC_INV_002_Product_Details.png
    ├── TC_CRT_002_Multiple_Products_Cart.png
    ├── TC_CHK_001_Checkout_Step1.png
    ├── TC_CHK_009_Order_Success.png
    └── TC_SEC_001_Direct_URL_Access.png
```

---

## 📑 Deliverables Overview

| Artifact | File Path | Purpose |
| :--- | :--- | :--- |
| **Test Plan** | [`Test-Plan/TestPlan.md`](Test-Plan/TestPlan.md) | Defines testing scope, objectives, strategy, environment setup, risk mitigation, and entry/exit criteria. |
| **Test Scenarios** | [`Test-Scenarios/TestScenarios.md`](Test-Scenarios/TestScenarios.md) | High-level test conditions covering user journeys and feature modules. |
| **Test Cases** | [`Test-Cases/TestCases.xlsx`](Test-Cases/TestCases.xlsx) | 38 granular test cases with ID, Title, Preconditions, Steps, Test Data, Expected Result, Actual Result, Status, and Priority. |
| **Bug Reports** | [`Bug-Reports/BugReport.xlsx`](Bug-Reports/BugReport.xlsx) | Production-ready defect template with fields for Severity, Priority, Steps to Reproduce, and Environment. |
| **Execution Tracker** | [`Test-Execution/TestExecutionReport.xlsx`](Test-Execution/TestExecutionReport.xlsx) | Matrix to record live test execution results, date, tester signature, and execution metrics. |
| **Test Summary Report**| [`Test-Summary/TestSummaryReport.md`](Test-Summary/TestSummaryReport.md) | Quality report with **8/38 executed**, pass rate, screenshot index, and recommendations. |
| **Test Data** | [`Test-Data/TestData.md`](Test-Data/TestData.md) | Documented test data suites (valid/invalid credentials, edge case inputs, postal codes). |

---

## 🎯 Test Coverage Breakup (38 Test Cases)

| Feature Module | Test Case Range | Positive | Negative | Boundary / Edge | UI & Security |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Authentication & Login** | `TC_LOG_001` - `TC_LOG_008` | 1 | 5 | 2 | 0 |
| **Product Listing & Detail** | `TC_INV_001` - `TC_INV_003` | 2 | 0 | 0 | 1 |
| **Product Sorting** | `TC_SRT_001` - `TC_SRT_004` | 4 | 0 | 0 | 0 |
| **Shopping Cart** | `TC_CRT_001` - `TC_CRT_006` | 6 | 0 | 0 | 0 |
| **Checkout Workflow** | `TC_CHK_001` - `TC_CHK_011` | 6 | 4 | 0 | 1 |
| **Navigation & App Menu** | `TC_NAV_001` - `TC_NAV_004` | 3 | 0 | 1 | 0 |
| **Security & Direct Access** | `TC_SEC_001` - `TC_SEC_003` | 0 | 0 | 1 | 2 |
| **TOTAL** | **38 Test Cases** | **22** | **9** | **4** | **3** |

*Executed in this cycle (by module): Login 2/8, Product Listing 2/3, Cart 1/6, Checkout 2/11, Security 1/3; Sorting and Navigation not yet executed.*

---

## 🚀 How to Execute Tests Manually

1. **Open Application**: Navigate to [https://www.saucedemo.com/](https://www.saucedemo.com/) using Google Chrome or Mozilla Firefox.
2. **Review Test Cases**: Open [`Test-Cases/TestCases.xlsx`](Test-Cases/TestCases.xlsx) or [`TestCases.csv`](Test-Cases/TestCases.csv).
3. **Execute Steps**: Follow the precise sequence of steps defined under `Test Steps` for each Test ID (`TC_LOG_001` to `TC_SEC_003`).
4. **Record Results**:
   - Update `Actual Result` and `Status` (`Pass` / `Fail`) in [`Test-Execution/TestExecutionReport.xlsx`](Test-Execution/TestExecutionReport.xlsx) or the CSV mirror.
   - If a test fails, log the defect in [`Bug-Reports/BugReport.xlsx`](Bug-Reports/BugReport.xlsx) and save screenshot evidence in [`Screenshots/`](Screenshots/README.md).
5. **Finalize Summary**: Keep [`Test-Summary/TestSummaryReport.md`](Test-Summary/TestSummaryReport.md) aligned with execution data and screenshot evidence.

---

## 🛠️ Tools & Skills Demonstrated

* **Methodologies**: Software Testing Life Cycle (STLC), Defect Life Cycle, Manual Testing.
* **Test Design Techniques**: Equivalence Partitioning (EP), Boundary Value Analysis (BVA), Error Guessing.
* **Documentation Standards**: IEEE 829 Test Planning Format, Standardized Defect Severity/Priority Matrix.
* **Tools**: Microsoft Excel / CSV Spreadsheets, Markdown, GitHub Version Control.

---

## 💡 Resume Project Highlights for QA Interviews

* "Designed a **38 test case** manual suite for SauceDemo and **executed 8 critical scenarios with 100% pass rate**, backed by named screenshot evidence in the repository."
* "Validated **authentication** (standard and locked-out user), **inventory and product detail** pages, **multi-item cart state**, **checkout step-one and order completion**, and **unauthenticated URL access** control."
* "Maintained full STLC artifacts—**Test Plan**, **Test Scenarios**, **Execution Tracker**, and **Test Summary Report**—suitable for fresher QA portfolio review."

---
*Created by Senior QA Engineer for portfolio verification.*
