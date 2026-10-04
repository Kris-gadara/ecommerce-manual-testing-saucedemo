# Test Data Specifications: SauceDemo E-Commerce Manual Testing

---

## Overview

This document provides all standardized test data suites utilized during the manual execution of test cases on **SauceDemo** (`https://www.saucedemo.com/`).

---

## 1. User Authentication Data Suite

| Profile Category | Username | Password | Purpose / Expected Behavior |
| :--- | :--- | :--- | :--- |
| **Standard User** | `standard_user` | `secret_sauce` | Normal active user. All workflows operate smoothly. |
| **Locked Out User** | `locked_out_user` | `secret_sauce` | Account locked. Should trigger locked out error banner. |
| **Problem User** | `problem_user` | `secret_sauce` | Defect testing. Triggers broken images and form field override issues. |
| **Performance Glitch User** | `performance_glitch_user` | `secret_sauce` | Performance testing. Simulates 3-5 second server response delay. |
| **Error User** | `error_user` | `secret_sauce` | Functional error testing. Buttons fail to trigger expected events. |
| **Visual User** | `visual_user` | `secret_sauce` | Visual layout testing. Elements misaligned or shifted. |
| **Invalid Password** | `standard_user` | `invalid_pass_123` | Password error validation. |
| **Invalid Username** | `non_existent_user` | `secret_sauce` | Username mismatch error validation. |

---

## 2. Inventory Product Data Catalog

| Item ID | Product Name | Catalog Price | Expected Image Name | Description Highlights |
| :--- | :--- | :--- | :--- | :--- |
| `item_4` | Sauce Labs Backpack | $29.99 | `sauce-backpack-1200x1500.jpg` | Carry all the things with sleek stream-lined pack |
| `item_0` | Sauce Labs Bike Light | $9.99 | `bike-light-1200x1500.jpg` | A red light with 3 protective modes |
| `item_1` | Sauce Labs Bolt T-Shirt | $15.99 | `bolt-shirt-1200x1500.jpg` | Get your testing superhero on with bolt shirt |
| `item_5` | Sauce Labs Fleece Jacket | $49.99 | `sauce-pullover-1200x1500.jpg` | It's not every day that you come across fleece |
| `item_2` | Sauce Labs Onesie | $7.99 | `red-onesie-1200x1500.jpg` | Rib snap infant onesie for junior developer |
| `item_3` | Test.allTheThings() T-Shirt (Red) | $15.99 | `red-tatt-1200x1500.jpg` | Classic Sauce Labs t-shirt in red |

---

## 3. Checkout Information Input Suites

### 3.1 Positive Checkout Data
- **First Name**: `John`
- **Last Name**: `Doe`
- **Zip / Postal Code**: `90210`

### 3.2 Negative / Boundary Test Suites
| Suite | First Name | Last Name | Postal Code | Expected Field Validation Error |
| :--- | :--- | :--- | :--- | :--- |
| **Blank First Name** | `[EMPTY]` | `Doe` | `90210` | `Error: First Name is required` |
| **Blank Last Name** | `John` | `[EMPTY]` | `90210` | `Error: Last Name is required` |
| **Blank Postal Code** | `John` | `Doe` | `[EMPTY]` | `Error: Postal Code is required` |
| **All Blank** | `[EMPTY]` | `[EMPTY]` | `[EMPTY]` | `Error: First Name is required` |
| **Special Characters** | `@#$!%` | `!@#$$` | `%!@#$` | Accepted or sanitized depending on requirement |
| **Long String (BVA)** | `A` * 100 chars | `B` * 100 chars | `90210123456789` | Form handling without visual breakage |

---

## 4. Protected Page URLs for Direct Access Security Testing

- `https://www.saucedemo.com/inventory.html`
- `https://www.saucedemo.com/cart.html`
- `https://www.saucedemo.com/checkout-step-one.html`
- `https://www.saucedemo.com/checkout-step-two.html`
- `https://www.saucedemo.com/checkout-complete.html`

---
*Maintained for QA Test Execution.*
