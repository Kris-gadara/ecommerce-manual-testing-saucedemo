# Test Summary Report: SauceDemo E-Commerce Manual Testing

---

## 1. Document Information

| Project Name | SauceDemo E-Commerce Manual Testing |
| :--- | :--- |
| **Application Under Test** | [SauceDemo](https://www.saucedemo.com/) |
| **Testing Cycle** | Manual Test Execution Phase |
| **Report Status** | **Partial Execution Complete (8 of 38 test cases)** |
| **Execution Date** | 5 October 2026 |
| **QA Lead / Tester** | [Your Name] |

---

## 2. Executive Summary

Manual test execution has been performed on **SauceDemo** with screenshot evidence captured for **8 test cases** covering login, product browsing, multi-item cart behavior, checkout entry, order completion, and unauthenticated URL access.

All **8 executed test cases passed**. Results align with expected application behavior shown in the files under `Screenshots/`. The remaining **30 test cases** in the suite are still pending execution; preparation artifacts (Test Plan, Scenarios, full Test Case catalog, and defect templates) remain available for continued testing.

---

## 3. Scope of Testing Executed

| Feature Module | Planned Test Cases | Executed | Passed | Failed | Blocked | Pending |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **Authentication & Login** | 8 | 2 | 2 | 0 | 0 | 6 |
| **Product Listing & Detail** | 3 | 2 | 2 | 0 | 0 | 1 |
| **Product Sorting** | 4 | 0 | 0 | 0 | 0 | 4 |
| **Shopping Cart** | 6 | 1 | 1 | 0 | 0 | 5 |
| **Checkout Workflow (Step 1 & 2)** | 11 | 2 | 2 | 0 | 0 | 9 |
| **Navigation Menu & State** | 4 | 0 | 0 | 0 | 0 | 4 |
| **Security & Edge Cases** | 3 | 1 | 1 | 0 | 0 | 2 |
| **TOTAL** | **38** | **8** | **8** | **0** | **0** | **30** |

---

## 4. Test Execution Metrics

```text
+-------------------------------------------------------------+
| TEST EXECUTION METRICS DASHBOARD                            |
+-------------------------------------------------------------+
| Total Test Cases Planned   : 38                             |
| Total Test Cases Executed  : 8 (21.1%)                      |
| Passed Test Cases          : 8                              |
| Failed Test Cases          : 0                              |
| Blocked Test Cases         : 0                              |
| Execution Pass Rate        : 100% (of executed tests)       |
+-------------------------------------------------------------+
```

---

## 5. Executed Test Cases (Screenshot Evidence)

| Test Case ID | Result | Screenshot | Observed Outcome |
| :--- | :---: | :--- | :--- |
| **TC_LOG_001** | Pass | `TC_LOG_001_Valid_Login.png` | After valid login, user lands on `inventory.html` with the Products page (catalog, sort control, cart icon). |
| **TC_LOG_002** | Pass | `TC_LOG_002_Locked_User.png` | Login with `locked_out_user` shows: *Epic sadface: Sorry, this user has been locked out.* |
| **TC_INV_001** | Pass | `TC_INV_001_Inventory_Page.png` | Inventory displays six products with images, descriptions, prices, **Add to cart** actions, and **Name (A to Z)** sort. |
| **TC_INV_002** | Pass | `TC_INV_002_Product_Details.png` | Product detail page for **Sauce Labs Backpack** ($29.99) with description, **Add to cart**, and **Back to products**. |
| **TC_CRT_002** | Pass | `TC_CRT_002_Multiple_Products_Cart.png` | Three products added; cart badge shows **3**; added items show **Remove** on the inventory page. |
| **TC_CHK_001** | Pass | `TC_CHK_001_Checkout_Step1.png` | **Checkout: Your Information** page loads (`checkout-step-one.html`) with First Name, Last Name, Zip/Postal Code, Cancel, and Continue; cart count **3**. |
| **TC_CHK_009** | Pass | `TC_CHK_009_Order_Success.png` | Order completes on `checkout-complete.html` with *Thank you for your order!* and **Back Home** / **Generate PDF order** actions. |
| **TC_SEC_001** | Pass | `TC_SEC_001_Direct_URL_Access.png` | Direct access to inventory without login shows: *Epic sadface: You can only access '/inventory.html' when you are logged in.* |

Detailed row-level status is recorded in [`Test-Execution/TestExecutionReport.csv`](../Test-Execution/TestExecutionReport.csv).

---

## 6. Defect Summary

No defects were logged during this execution cycle. All observed behavior for the 8 executed tests matched expected results.

| Defect ID | Summary | Module | Severity | Priority | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| — | No defects logged for executed tests | — | — | — | — |

### Defect Severity Distribution:
- **Critical (S1)**: 0 logged
- **High (S2)**: 0 logged
- **Medium (S3)**: 0 logged
- **Low (S4)**: 0 logged

---

## 7. Recommendations & Quality Assessment

1. **Completed coverage**: Core happy-path flows validated with evidence—authentication (valid and locked-out user), inventory and product detail views, multi-item cart state, checkout step-one navigation, successful order completion, and session protection on direct inventory URL access.
2. **Remaining work**: Execute the **30 pending** test cases (sorting, cart edge cases, checkout validation, navigation menu, additional security/edge scenarios) and update [`Test-Execution/TestExecutionReport.csv`](../Test-Execution/TestExecutionReport.csv) accordingly.
3. **Defect tracking**: If failures are found in future runs, log them in `Bug-Reports/BugReport.xlsx` and attach supporting screenshots in `Screenshots/`.

**Quality note (executed scope only):** SauceDemo behaved consistently with documented expectations for the scenarios above. No functional issues were observed in the executed subset.

---
*Prepared for QA portfolio presentation — partial execution with screenshot evidence.*
