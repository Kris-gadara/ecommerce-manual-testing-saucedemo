# Test Scenarios: SauceDemo E-Commerce Manual Testing

---

## Overview

Test Scenarios represent high-level test conditions derived from business requirements and user workflows of the **SauceDemo** application. Each scenario maps to one or more detailed Test Cases in `Test-Cases/TestCases.xlsx`.

---

## 1. Authentication & Session Scenarios (TS_LOG)

| Scenario ID | Test Scenario Description | Coverage | Test Case Mapping |
| :--- | :--- | :--- | :--- |
| **TS_LOG_01** | Verify user authentication with valid standard user credentials | Positive | `TC_LOG_001` |
| **TS_LOG_02** | Verify authentication failure with locked-out account credentials | Negative | `TC_LOG_002` |
| **TS_LOG_03** | Verify authentication failure with invalid username or password | Negative | `TC_LOG_003` |
| **TS_LOG_04** | Verify form validation when required login fields are left blank | Validation | `TC_LOG_004`, `TC_LOG_005`, `TC_LOG_006` |
| **TS_LOG_05** | Verify system behavior under problematic and delayed user profiles | Edge / Performance | `TC_LOG_007`, `TC_LOG_008` |

---

## 2. Product Catalog & Listing Scenarios (TS_INV)

| Scenario ID | Test Scenario Description | Coverage | Test Case Mapping |
| :--- | :--- | :--- | :--- |
| **TS_INV_01** | Verify inventory page catalog grid display and visual elements post-login | UI / Functional | `TC_INV_001` |
| **TS_INV_02** | Verify navigation and content accuracy on Product Detail Page (PDP) | Functional | `TC_INV_002` |
| **TS_INV_03** | Verify catalog navigation return flow via 'Back to products' button | Functional | `TC_INV_003` |

---

## 3. Product Sorting & Filtering Scenarios (TS_SRT)

| Scenario ID | Test Scenario Description | Coverage | Test Case Mapping |
| :--- | :--- | :--- | :--- |
| **TS_SRT_01** | Verify catalog sorting in alphabetical ascending order (Name A to Z) | Functional | `TC_SRT_001` |
| **TS_SRT_02** | Verify catalog sorting in alphabetical descending order (Name Z to A) | Functional | `TC_SRT_002` |
| **TS_SRT_03** | Verify catalog sorting in numerical price ascending order (Price Low to High) | Functional | `TC_SRT_003` |
| **TS_SRT_04** | Verify catalog sorting in numerical price descending order (Price High to Low) | Functional | `TC_SRT_004` |

---

## 4. Shopping Cart Scenarios (TS_CRT)

| Scenario ID | Test Scenario Description | Coverage | Test Case Mapping |
| :--- | :--- | :--- | :--- |
| **TS_CRT_01** | Verify adding single and multiple items to shopping cart from catalog | Functional | `TC_CRT_001`, `TC_CRT_002` |
| **TS_CRT_02** | Verify removing items from shopping cart on inventory and cart pages | Functional | `TC_CRT_003`, `TC_CRT_005` |
| **TS_CRT_03** | Verify shopping cart badge counter dynamic update accuracy | Functional / UI | `TC_CRT_001`, `TC_CRT_002`, `TC_CRT_003`, `TC_CRT_005` |
| **TS_CRT_04** | Verify 'Continue Shopping' functionality from Cart page | Functional | `TC_CRT_006` |

---

## 5. Checkout & Order Placement Scenarios (TS_CHK)

| Scenario ID | Test Scenario Description | Coverage | Test Case Mapping |
| :--- | :--- | :--- | :--- |
| **TS_CHK_01** | Verify navigation and entry into Checkout Step 1 ('Your Information') | Functional | `TC_CHK_001` |
| **TS_CHK_02** | Verify user information submission with valid customer data | Positive | `TC_CHK_002` |
| **TS_CHK_03** | Verify field validation for missing First Name, Last Name, or Postal Code | Validation | `TC_CHK_003`, `TC_CHK_004`, `TC_CHK_005` |
| **TS_CHK_04** | Verify subtotal, tax calculation (8%), and grand total on Checkout Overview | Mathematical | `TC_CHK_007` |
| **TS_CHK_05** | Verify final order completion flow and success screen presentation | Functional | `TC_CHK_009`, `TC_CHK_010` |
| **TS_CHK_06** | Verify workflow cancellation at Step 1 and Step 2 | Functional | `TC_CHK_006`, `TC_CHK_011` |

---

## 6. Navigation, Security & Edge Scenarios (TS_NAV / TS_SEC)

| Scenario ID | Test Scenario Description | Coverage | Test Case Mapping |
| :--- | :--- | :--- | :--- |
| **TS_NAV_01** | Verify sidebar menu interaction and option links | UI / Functional | `TC_NAV_001`, `TC_NAV_002` |
| **TS_NAV_02** | Verify app state reset functionality clearing cart and item states | State Reset | `TC_NAV_003` |
| **TS_NAV_03** | Verify secure user logout ending active session | Security | `TC_NAV_004` |
| **TS_SEC_01** | Verify unauthenticated direct URL access prevention to protected pages | Security | `TC_SEC_001` |
| **TS_SEC_02** | Verify browser history back button behavior after logging out | Security | `TC_SEC_002` |
| **TS_SEC_03** | Verify edge case behavior when initiating checkout with 0 items in cart | Boundary / Edge | `TC_SEC_003` |

---
*Created for manual testing traceability and verification.*
