# Portfolio: QA Manual Testing Baseline — Sauce Demo (Swag Labs)

## 📌 Project Overview
This repository documents the manual functional testing for the **Sauce Demo** (Swag Labs) e-commerce production website. Since the application lacked pre-existing documentation, I reverse-engineered its business rules to establish a clean QA testing baseline, map out user personas, and capture critical flow blockers before they impact the live user experience.

The core deliverables are structured into two main tracking workbooks:
* 📁 **[Test Plan & Test Cases](./Test_Cases_and_Test_Execution.xlsx)** — Full test coverage split by primary business modules.
* 📁 **[Bug Report](./Bug_Report.xlsx)** — Lifecycle logging and technical details of functional edge-cases discovered during execution.

---

## 📊 Test Execution Summary
I designed and executed **40 distinct test cases** covering positive paths, boundary conditions, and negative validations across 4 primary modules:

| Module Name | Total Cases | Passed | Failed | Pass Rate |
| :--- | :---: | :---: | :---: | :---: |
| **User Login** | 13 | 13 | 0 | 100% |
| **Product Catalog & Sorting** | 7 | 7 | 0 | 100% |
| **Shopping Cart Mechanics** | 11 | 10 | 1 | 90.9% |
| **Checkout Workflow** | 9 | 8 | 1 | 88.8% |
| **Total** | **40** | **38** | **2** | **95%** |

---

## 🚨 Logged Defects (Highlights)
During the execution cycle, **2 functional bugs** were isolated, prioritized, and tracked with detailed reproduction steps:

### 🎯 [BUG-CH-001] Empty Cart Checkout Validation Bypass
* **Module:** Checkout (`TC-CH-001`)
* **Severity:** `Critical` | **Priority:** `P1`
* **The Issue:** The application lacks a zero-state validator on the cart page, allowing users to bypass standard flow logic and proceed directly to the `/checkout-step-one.html` screen even with 0 items in their cart.
* **Business Risk:** High logical conflict that could disrupt downstream payment processing and inventory validation.

### 🎯 [BUG-C-001] Quantity Modification Lock in Cart
* **Module:** Cart Functionality (`TC-C-002`)
* **Severity:** `High` | **Priority:** `P2`
* **The Issue:** The cart UI does not support duplicate line item increments or multi-quantity selection for the same product ID.
* **Business Risk:** Restricts bulk orders, directly impacting user conversion and reducing potential average order value (AOV).

---

## 🛠️ Approach & Core Capabilities
* **Testing Types:** Black Box Testing, Exploratory Testing, Negative & Boundary Value Testing.
* **User Persona Validation:** Validated application stability across distinct simulated behaviors (Standard User, Locked Out User, Performance Glitched, and Visual Anomalies).
* **Environment:** Google Chrome | Windows 10.

---
*Maintained by Agamita Sasya*
