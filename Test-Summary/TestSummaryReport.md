# Test Summary Report: SauceDemo E-Commerce Manual Testing

---

## 1. Document Information

| Project Name | SauceDemo E-Commerce Manual Testing |
| :--- | :--- |
| **Application Under Test** | [SauceDemo](https://www.saucedemo.com/) |
| **Testing Cycle** | Manual Test Execution Phase — **Complete** |
| **Report Status** | **All 38 test cases executed** |
| **Execution Date** | 5 October 2026 |
| **QA Lead / Tester** | [Krish Gadara] |

---

## 2. Executive Summary

Manual testing of the **full SauceDemo test suite (38 test cases)** has been completed. Test conditions span authentication, product listing and detail, sorting, shopping cart, checkout, navigation, and security/edge scenarios as defined in the Test Plan and Test Cases deliverables.

**Execution proof:** Eight **representative screenshots** are stored under `Screenshots/`. These files are **sample evidence for portfolio review**—they illustrate key flows and trace to specific test case IDs. They do **not** represent the number of tests executed; all 38 cases were run, with row-level outcomes recorded in [`Test-Execution/TestExecutionReport.csv`](../Test-Execution/TestExecutionReport.csv) and `TestExecutionReport.xlsx`.

---

## 3. Scope of Testing Executed

All planned test cases in each module were executed during this cycle.

| Feature Module | Planned Test Cases | Executed |
| :--- | :---: | :---: |
| **Authentication & Login** | 8 | 8 |
| **Product Listing & Detail** | 3 | 3 |
| **Product Sorting** | 4 | 4 |
| **Shopping Cart** | 6 | 6 |
| **Checkout Workflow (Step 1 & 2)** | 11 | 11 |
| **Navigation Menu & State** | 4 | 4 |
| **Security & Edge Cases** | 3 | 3 |
| **TOTAL** | **38** | **38** |

**Pass / Fail / Blocked counts:** Documented per test case in the Test Execution Report (`Test-Execution/TestExecutionReport.csv` / `.xlsx`). This summary does not duplicate those metrics here so the execution tracker remains the single source of truth.

---

## 4. Test Execution Metrics

```text
+-------------------------------------------------------------+
| TEST EXECUTION METRICS DASHBOARD                            |
+-------------------------------------------------------------+
| Total Test Cases Planned   : 38                             |
| Total Test Cases Executed  : 38 (100%)                      |
| Pass / Fail / Blocked      : See Test Execution Report      |
| Screenshot proof samples   : 8 (representative evidence)    |
+-------------------------------------------------------------+
```

---

## 5. Screenshot Proof Samples (Representative Evidence)

The following eight images are attached as **execution proof samples**. Additional cases were executed without a dedicated screenshot in this repository.

| Linked test case | Screenshot file | What the sample shows |
| :--- | :--- | :--- |
| **TC_LOG_001** | `TC_LOG_001_Valid_Login.png` | Products page at `inventory.html` after successful login (catalog, sort, cart). |
| **TC_LOG_002** | `TC_LOG_002_Locked_User.png` | Locked-out login error: *Sorry, this user has been locked out.* |
| **TC_INV_001** | `TC_INV_001_Inventory_Page.png` | Full inventory grid with prices and **Add to cart** actions. |
| **TC_INV_002** | `TC_INV_002_Product_Details.png` | Sauce Labs Backpack detail page with **Back to products**. |
| **TC_CRT_002** | `TC_CRT_002_Multiple_Products_Cart.png` | Three items in cart; badge **3**; **Remove** on added lines. |
| **TC_CHK_001** | `TC_CHK_001_Checkout_Step1.png` | **Checkout: Your Information** (`checkout-step-one.html`). |
| **TC_CHK_009** | `TC_CHK_009_Order_Success.png` | Order complete: *Thank you for your order!* on `checkout-complete.html`. |
| **TC_SEC_001** | `TC_SEC_001_Direct_URL_Access.png` | Login required when accessing inventory without a session. |

Images are located in [`Screenshots/`](../Screenshots/) and embedded in the project [`README.md`](../README.md) for portfolio presentation.

---

## 6. Defect Summary

Defect logging uses [`Bug-Reports/BugReport.csv`](../Bug-Reports/BugReport.csv) / `BugReport.xlsx`. Refer to those files for defect IDs, severity, priority, and status for issues found during execution.

| Defect ID | Summary | Module | Severity | Priority | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| *(see Bug Report)* | *(see Bug Report)* | *(see Bug Report)* | *(see Bug Report)* | *(see Bug Report)* | *(see Bug Report)* |

---

## 7. Recommendations & Quality Assessment

1. **Execution complete:** The defined 38-case suite for SauceDemo has been executed end-to-end; maintain the Test Execution Report as the authoritative record for each case’s status and notes.
2. **Evidence:** Use the **8 screenshot samples** for demos and interviews; they cover critical paths (login, catalog, cart, checkout completion, session security) without replacing the full written execution log.
3. **Regression:** For future SauceDemo releases, re-run the same suite and refresh execution data and proof samples as needed.

---
*Prepared for fresher QA portfolio presentation — full suite executed with representative screenshot proof.*
