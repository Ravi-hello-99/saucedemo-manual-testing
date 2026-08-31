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
| Passed | 35 |
| Failed | 10 |
| Pass Rate | 78% |

All test cases on the `standard_user` account passed, confirming the core login, inventory, cart, checkout, and logout flows work correctly. All 10 failures were found on the `problem_user` account, a test account intentionally built with defects for QA practice.

## Key Bugs Found

| Bug ID | Module | Bug Summary | Severity |
|---|---|---|---|
| BUG_001 | Inventory | Product images are incorrect/mismatched — all products show the same wrong image | Medium |
| BUG_002 | Inventory | Sorting by "Name (Z to A)" does not reorder products | High |
| BUG_003 | Inventory | Sorting by "Price (low to high)" does not reorder products | High |
| BUG_004 | Checkout | Checkout form does not reliably accept typed text input, blocking order completion | Critical |

Full bug reports (steps to reproduce, expected vs actual result, impact) are documented in [`BUGS.md`](./BUGS.md), with supporting screenshots in the `Bugs_Screenshots/` folder.

## Tools Used

- **Test Design & Execution:** Microsoft Excel / Google Sheets
- **Application:** SauceDemo (web-based demo app)
- **Browser:** Google Chrome

## Repository Contents

```
saucedemo-manual-testing/
│
├── SauceDemo_Manual_Testcases1-45.xlsx   → Full test case sheet (45 test cases, executed with results)
├── BUGS.md                                → Formal bug reports for all verified defects
├── Bugs_Screenshots/                      → Screenshots proving each documented bug
└── README.md                              → This file
```

## What This Project Demonstrates

- Writing clear, structured test cases covering positive, negative, boundary, and security scenarios
- Executing tests methodically across multiple modules and user accounts
- Verifying results with evidence (screenshots) before reporting a defect
- Identifying and accurately documenting real functional defects
- Distinguishing between application-level bugs and expected/simulated behavior
- Attention to detail in comparing expected vs actual results

## Related Project

This manual testing effort is paired with a Selenium automation project covering the same application:
[saucedemo-selenium-framework](https://github.com/Ravi-hello-99/saucedemo-selenium-framework)

---

*This project is part of my QA testing portfolio. Feedback and suggestions are welcome!*
