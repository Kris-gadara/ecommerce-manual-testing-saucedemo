# Test Summary Report: SauceDemo E-Commerce Manual Testing

---

## 1. Document Information

| Project Name               | SauceDemo E-Commerce Manual Testing                       |
| :------------------------- | :-------------------------------------------------------- |
| **Application Under Test** | [SauceDemo](https://www.saucedemo.com/)                   |
| **Testing Cycle**          | QA Evidence Review and Result Adjudication — **Complete** |
| **Report Status**          | **39 results finalized: 37 Pass, 2 Fail**                 |
| **Review Dates**           | 5–6 October 2026                                          |
| **QA Reviewer**            | QA Review                                                 |

---

## 2. Executive Summary

The project records contain **39 unique test cases** (the previous project-level total of 38 was incorrect). Final statuses have been assigned to all 39 cases: **37 Pass and 2 Fail**. The review covered authentication, product listing and detail, sorting, shopping cart, checkout, navigation, and security/edge scenarios.

**Evidence basis:** Eight representative screenshots in `Screenshots/` support the linked test cases. Remaining results are QA judgments based on the supplied test steps, expected behavior, known SauceDemo behavior, and existing project records; they are not represented as fresh manual executions. The row-level status and evidence basis are recorded in [`Test-Execution/TestExecutionReport.csv`](../Test-Execution/TestExecutionReport.csv) and `TestExecutionReport.xlsx`.

---

## 3. Scope Reviewed

All planned cases were reviewed and assigned a final Pass or Fail status.

| Feature Module                     | Test Cases | Results Finalized |
| :--------------------------------- | :--------: | :---------------: |
| **Authentication & Login**         |     8      |         8         |
| **Product Listing & Detail**       |     3      |         3         |
| **Product Sorting**                |     4      |         4         |
| **Shopping Cart**                  |     6      |         6         |
| **Checkout Workflow (Step 1 & 2)** |     11     |        11         |
| **Navigation Menu & State**        |     4      |         4         |
| **Security & Edge Cases**          |     3      |         3         |
| **TOTAL**                          |   **39**   |      **39**       |

**Pass / Fail / Blocked counts:** Documented per test case in the Test Execution Report (`Test-Execution/TestExecutionReport.csv` / `.xlsx`). This summary does not duplicate those metrics here so the execution tracker remains the single source of truth.

---

## 4. Test Execution Metrics

```text
+-------------------------------------------------------------+
| TEST EXECUTION METRICS DASHBOARD                            |
+-------------------------------------------------------------+
| Total Test Cases           : 39                             |
| Final Pass / Fail          : 37 Pass / 2 Fail               |
| Pending                    : 0                              |
| Screenshot proof samples   : 8 (representative evidence)    |
+-------------------------------------------------------------+
```

---

## 5. Screenshot Proof Samples (Representative Evidence)

The following eight images are attached as **case-specific evidence samples**. Other cases were assigned a QA judgment from the project records without a dedicated screenshot.

| Linked test case | Screenshot file                         | What the sample shows                                                           |
| :--------------- | :-------------------------------------- | :------------------------------------------------------------------------------ |
| **TC_LOG_001**   | `TC_LOG_001_Valid_Login.png`            | Products page at `inventory.html` after successful login (catalog, sort, cart). |
| **TC_LOG_002**   | `TC_LOG_002_Locked_User.png`            | Locked-out login error: _Sorry, this user has been locked out._                 |
| **TC_INV_001**   | `TC_INV_001_Inventory_Page.png`         | Full inventory grid with prices and **Add to cart** actions.                    |
| **TC_INV_002**   | `TC_INV_002_Product_Details.png`        | Sauce Labs Backpack detail page with **Back to products**.                      |
| **TC_CRT_002**   | `TC_CRT_002_Multiple_Products_Cart.png` | Three items in cart; badge **3**; **Remove** on added lines.                    |
| **TC_CHK_001**   | `TC_CHK_001_Checkout_Step1.png`         | **Checkout: Your Information** (`checkout-step-one.html`).                      |
| **TC_CHK_009**   | `TC_CHK_009_Order_Success.png`          | Order complete: _Thank you for your order!_ on `checkout-complete.html`.        |
| **TC_SEC_001**   | `TC_SEC_001_Direct_URL_Access.png`      | Login required when accessing inventory without a session.                      |

Images are located in [`Screenshots/`](../Screenshots/) and embedded in the project [`README.md`](../README.md) for portfolio presentation.

---

## 6. Defect Summary

Defect logging uses [`Bug-Reports/BugReport.csv`](../Bug-Reports/BugReport.csv) / `BugReport.xlsx`. Refer to those files for defect IDs, severity, priority, and status for issues found during execution.

| Defect ID | Summary                                         | Module          | Severity | Priority | Status                            |
| :-------- | :---------------------------------------------- | :-------------- | :------- | :------- | :-------------------------------- |
| BUG_001   | Problem user displays duplicated product images | Product Listing | Medium   | Medium   | Open; linked to TC_LOG_007 (Fail) |
| BUG_002   | Checkout allows an empty cart to be completed   | Checkout        | Low      | Low      | Open; linked to TC_SEC_003 (Fail) |

---

## 7. Recommendations & Quality Assessment

1. **Results complete:** The 39-case suite has final statuses and defect links in the Test Execution Report; use it as the record of the QA adjudication.
2. **Evidence:** The **8 screenshot samples** support key paths (login, catalog, cart, checkout completion, session security). They do not provide case-specific proof for every result.
3. **Regression:** For a formal release sign-off, freshly execute all 39 cases and capture evidence for the currently judgment-based results.

---

_Prepared for QA portfolio review — all 39 results adjudicated with representative screenshot evidence._
