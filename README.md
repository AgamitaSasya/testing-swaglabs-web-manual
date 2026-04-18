# Manual Testing Portfolio: Sauce Demo (Swag Labs)

## Project Overview
This project documents the manual functional testing of the **Sauce Demo** (Swag Labs) e-commerce website https://www.saucedemo.com/ . The primary objective was to validate the end-to-end user from secure authentication to product management and final checkout ensuring a bug free experience for users.

I have structured the documentation into two main workbooks for better traceability:
* **[Test Plan & Test Cases](./Test_Cases.xlsx)**: Includes the Requirement Traceability Matrix (RTM), Test Scenarios, and 25 detailed Test Cases.
* **[Test Execution & Bug Report](./Test_Execution_and_Bug_Report.xlsx)**: Documents the actual results of the execution, pass/fail status, and technical details of discovered defects.

## Test Execution Summary
A total of **25 test cases** were executed across the following modules:
| Module ID | Module Name | Total Cases | Passed | Failed |
| :--- | :--- | :---: | :---: | :---: |
| 1.1 | User Login | 5 | 5 | 0 |
| 1.2 | Catalog Product | 7 | 7 | 0 |
| 1.3 | Cart Functionality | 5 | 4 | 1 |
| 1.4 | Checkout Process | 6 | 5 | 1 |
| 1.5 | Navbar & Navigation | 2 | 2 | 0 |
| **Total** | | **25** | **23** | **2** |

## Defect Reports (Highlights)
During the test execution, **2 functional bugs** were identified and documented:

1. **[SWG_01] Quantity Limitation in Cart**
   - **Description:** Users are unable to add more than one unit of the same product to the shopping cart.
   - **Impact:** Prevents bulk purchases, potentially leading to lower sales conversion.
2. **[SWG_02] Empty Cart Checkout Bypass**
   - **Description:** The system allows users to proceed to the 'Checkout: Your Information' page even when the cart contains zero items.
   - **Impact:** Critical logical error that may cause system confusion during the payment phase.

## 🛠 Tools & Methodology
- **Testing Type:** Manual Testing (Black Box)
- **Techniques:** Boundary Value Analysis, Equivalence Partitioning, Positive & Negative Testing.
- **Tools:** Microsoft Excel (Test Management), Google Chrome (Test Environment).
- **Environment:** Windows 10 / Web Browser.

---
*Created by [Agamita Sasya]*
