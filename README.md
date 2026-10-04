# E-Commerce Website Manual Testing Portfolio Project

![QA Testing](https://img.shields.io/badge/QA-Manual%20Testing-blue.svg)
![Application](https://img.shields.io/badge/AUT-SauceDemo-orange.svg)
![Status](https://img.shields.io/badge/Status-Ready%20for%20Execution-brightgreen.svg)
![Test Cases](https://img.shields.io/badge/Test%20Cases-38%20Defined-success.svg)

A professional, interview-ready manual testing portfolio project built for the **SauceDemo** web application ([https://www.saucedemo.com/](https://www.saucedemo.com/)).

This repository demonstrates industry-standard Quality Assurance (QA) practices, including IEEE-style Test Planning, Scenario Mapping, 38 detailed Test Cases (covering Functional, Negative, Boundary, UI/UX, and Security aspects), Defect Reporting, and Execution Tracking templates.

---

## 📌 Application Under Test (AUT)

* **Application Name**: SauceDemo (Swag Labs)
* **URL**: [https://www.saucedemo.com/](https://www.saucedemo.com/)
* **Description**: A simulated e-commerce web application featuring authentication, product catalog display, sorting algorithms, cart state management, multi-step checkout workflow, and side menu management.

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
│   └── TestExecutionReport.csv         # CSV version for easy GitHub viewing
├── Test-Summary/
│   └── TestSummaryReport.md            # Final Test Summary & Quality Metrics Template
├── Test-Data/
│   └── TestData.md                     # Comprehensive Test Data Specifications
└── Screenshots/
    └── README.md                       # Guidelines for attaching Defect & Execution Screenshots
```

---

## 📑 Deliverables Overview

| Artifact | File Path | Purpose |
| :--- | :--- | :--- |
| **Test Plan** | [`Test-Plan/TestPlan.md`](file:///c:/K/Projects/ecommerce-manual-testing-saucedemo/ecommerce-manual-testing-saucedemo/Test-Plan/TestPlan.md) | Defines testing scope, objectives, strategy, environment setup, risk mitigation, and entry/exit criteria. |
| **Test Scenarios** | [`Test-Scenarios/TestScenarios.md`](file:///c:/K/Projects/ecommerce-manual-testing-saucedemo/ecommerce-manual-testing-saucedemo/Test-Scenarios/TestScenarios.md) | High-level test conditions covering user journeys and feature modules. |
| **Test Cases** | [`Test-Cases/TestCases.xlsx`](file:///c:/K/Projects/ecommerce-manual-testing-saucedemo/ecommerce-manual-testing-saucedemo/Test-Cases/TestCases.xlsx) | 38 granular test cases with ID, Title, Preconditions, Steps, Test Data, Expected Result, Actual Result, Status, and Priority. |
| **Bug Reports** | [`Bug-Reports/BugReport.xlsx`](file:///c:/K/Projects/ecommerce-manual-testing-saucedemo/ecommerce-manual-testing-saucedemo/Bug-Reports/BugReport.xlsx) | Production-ready defect template with fields for Severity, Priority, Steps to Reproduce, and Environment. |
| **Execution Tracker** | [`Test-Execution/TestExecutionReport.xlsx`](file:///c:/K/Projects/ecommerce-manual-testing-saucedemo/ecommerce-manual-testing-saucedemo/Test-Execution/TestExecutionReport.xlsx) | Matrix to record live test execution results, date, tester signature, and execution metrics. |
| **Test Summary Report**| [`Test-Summary/TestSummaryReport.md`](file:///c:/K/Projects/ecommerce-manual-testing-saucedemo/ecommerce-manual-testing-saucedemo/Test-Summary/TestSummaryReport.md) | Quality sign-off report outlining test completion status, metric summaries, and recommendations. |
| **Test Data** | [`Test-Data/TestData.md`](file:///c:/K/Projects/ecommerce-manual-testing-saucedemo/ecommerce-manual-testing-saucedemo/Test-Data/TestData.md) | Documented test data suites (valid/invalid credentials, edge case inputs, postal codes). |

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

---

## 🚀 How to Execute Tests Manually

1. **Open Application**: Navigate to [https://www.saucedemo.com/](https://www.saucedemo.com/) using Google Chrome or Mozilla Firefox.
2. **Review Test Cases**: Open [`Test-Cases/TestCases.xlsx`](file:///c:/K/Projects/ecommerce-manual-testing-saucedemo/ecommerce-manual-testing-saucedemo/Test-Cases/TestCases.xlsx) or [`TestCases.csv`](file:///c:/K/Projects/ecommerce-manual-testing-saucedemo/ecommerce-manual-testing-saucedemo/Test-Cases/TestCases.csv).
3. **Execute Steps**: Follow the precise sequence of steps defined under `Test Steps` for each Test ID (`TC_LOG_001` to `TC_SEC_003`).
4. **Record Results**:
   - Update `Actual Result` and `Status` (`Pass` / `Fail`) in [`Test-Execution/TestExecutionReport.xlsx`](file:///c:/K/Projects/ecommerce-manual-testing-saucedemo/ecommerce-manual-testing-saucedemo/Test-Execution/TestExecutionReport.xlsx).
   - If a test fails, log the defect in [`Bug-Reports/BugReport.xlsx`](file:///c:/K/Projects/ecommerce-manual-testing-saucedemo/ecommerce-manual-testing-saucedemo/Bug-Reports/BugReport.xlsx) and save screenshot evidence in [`Screenshots/`](file:///c:/K/Projects/ecommerce-manual-testing-saucedemo/ecommerce-manual-testing-saucedemo/Screenshots/README.md).
5. **Finalize Summary**: Update metrics in [`Test-Summary/TestSummaryReport.md`](file:///c:/K/Projects/ecommerce-manual-testing-saucedemo/ecommerce-manual-testing-saucedemo/Test-Summary/TestSummaryReport.md).

---

## 🛠️ Tools & Skills Demonstrated

* **Methodologies**: Software Testing Life Cycle (STLC), Defect Life Cycle, Manual Testing.
* **Test Design Techniques**: Equivalence Partitioning (EP), Boundary Value Analysis (BVA), Error Guessing.
* **Documentation Standards**: IEEE 829 Test Planning Format, Standardized Defect Severity/Priority Matrix.
* **Tools**: Microsoft Excel / CSV Spreadsheets, Markdown, GitHub Version Control.

---

## 💡 Resume Project Highlights for QA Interviews

* "Designed and executed a comprehensive manual testing suite of **38 test cases** for an e-commerce platform covering login, catalog sorting, shopping cart dynamics, multi-step checkout, and session security."
* "Prepared end-to-end STLC artifacts including **Test Plan**, **Test Scenarios**, **Boundary Value Analysis Test Cases**, **Defect Reports**, and **Execution Summary Reports**."
* "Identified edge cases such as unauthenticated direct URL access (`/inventory.html`), session back-button retention, and empty cart checkout behaviors."

---
*Created by Senior QA Engineer for portfolio verification.*
