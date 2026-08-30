# SauceDemo Manual Testing Project

Manual QA testing project performed on [SauceDemo](https://www.saucedemo.com) — a demo e-commerce web application built for test automation and manual testing practice.

This project demonstrates end-to-end manual testing skills: test case design, test execution, defect identification, and bug documentation, performed as part of my QA portfolio as a fresher seeking a Software Tester role.

## Project Overview

- **Application Under Test:** SauceDemo (https://www.saucedemo.com)
- **Testing Type:** Manual Functional Testing
- **Modules Covered:** Login, Inventory, Cart, Checkout, Logout, UI, Security
- **Total Test Cases:** 45
- **Test Accounts Used:** standard_user, locked_out_user, problem_user

## Test Execution Summary

| Metric | Count |
|---|---|
| Total Test Cases | 45 |
| Passed | 33 |
| Failed | 12 |
| Pass Rate | 73% |

## Key Bugs Found

| ID | Module | Bug Summary | Severity |
|---|---|---|---|
| TC_027 | Checkout | Leaving First Name blank shows "Last Name is required" error instead of "First Name is required" | High |
| TC_029 | Checkout | Leaving Zip Code blank shows "Last Name is required" error instead of "Postal Code is required" | High |
| TC_007 / TC_041 | Login / Inventory | Product images render incorrectly/mismatched when logged in as `problem_user` | Medium |
| TC_012–015 | Inventory | Product sorting (A-Z, Z-A, price low-high, high-low) does not reorder products when using `problem_user` | High |
| TC_030, TC_032–034 | Checkout | Checkout flow gets completely stuck and cannot be completed when using `problem_user` | High |

Full details for every test case (steps, test data, expected vs actual result) are available in the test case sheet below.

## Tools Used

- **Test Design & Execution:** Microsoft Excel / Google Sheets
- **Application:** SauceDemo (web-based demo app)
- **Browser:** Google Chrome

## Repository Contents

```
saucedemo-manual-testing/
│
├── SauceDemo_Manual_Testcases1-45.xlsx   → Full test case sheet (45 test cases, executed with results)
├── screenshots/                       → Screenshots of failed test cases / bugs found
└── README.md                          → This file
```

## What This Project Demonstrates

- Writing clear, structured test cases covering positive, negative, boundary, and security scenarios
- Executing tests methodically across multiple modules and user accounts
- Identifying and accurately documenting real functional defects
- Distinguishing between application-level bugs and expected/simulated behavior
- Attention to detail in comparing expected vs actual results

## Related Project

This manual testing effort is paired with a Selenium automation project covering the same application:
[saucedemo-selenium-framework](https://github.com/YOUR_USERNAME/saucedemo-selenium-framework)

---

*This project is part of my QA testing portfolio. Feedback and suggestions are welcome

