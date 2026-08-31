# Bug Reports — SauceDemo Manual Testing

All bugs below were found and verified using the `problem_user` account on [saucedemo.com](https://www.saucedemo.com). Screenshots are located in the `Bugs_Screenshots/` folder. The `standard_user` account was tested against the same scenarios and worked correctly in all cases, confirming these are account-specific defects.

---

## BUG_001 — Product images are incorrect on the Inventory page

**Test Case Reference:** TC_007 / TC_041
**Module:** Inventory
**Environment:** Chrome browser, saucedemo.com, `problem_user` account
**Severity:** Medium
**Priority:** Medium

**Steps to Reproduce:**
1. Log in with `problem_user` / `secret_sauce`
2. Observe the product images on the Inventory (Products) page

**Expected Result:**
Each of the 6 products should display its own correct, distinct image (backpack, bike light, T-shirt, jacket, etc.)

**Actual Result:**
All product images are replaced with the same incorrect image (a dog holding a tennis ball), regardless of the actual product.

**Screenshot:** `Bugs_Screenshots/TC_007_bug.png`

**Impact:**
Customers cannot visually identify products before purchase, which would significantly harm usability and trust in a real e-commerce setting.

---

## BUG_002 — Sorting by "Name (Z to A)" does not reorder products

**Test Case Reference:** TC_013
**Module:** Inventory
**Environment:** Chrome browser, saucedemo.com, `problem_user` account
**Severity:** High
**Priority:** High

**Steps to Reproduce:**
1. Log in with `problem_user` / `secret_sauce`
2. Click the sort dropdown (top right of Products page)
3. Select "Name (Z to A)"

**Expected Result:**
Products should reorder alphabetically from Z to A.

**Actual Result:**
Products remained in their original "Name (A to Z)" order — the sort had no effect.

**Screenshot:** `Bugs_Screenshots/TC_013_bug.png`

**Impact:**
Sorting is a core product-discovery feature; if it silently fails, users cannot find products in their preferred order, which is especially problematic in larger catalogs.

---

## BUG_003 — Sorting by "Price (low to high)" does not reorder products

**Test Case Reference:** TC_014
**Module:** Inventory
**Environment:** Chrome browser, saucedemo.com, `problem_user` account
**Severity:** High
**Priority:** High

**Steps to Reproduce:**
1. Log in with `problem_user` / `secret_sauce`
2. Click the sort dropdown (top right of Products page)
3. Select "Price (low to high)"

**Expected Result:**
Products should reorder from lowest to highest price.

**Actual Result:**
Products remained in their original "Name (A to Z)" order — price sorting had no effect.

**Screenshot:** `Bugs_Screenshots/TC_014_bug.png`

**Impact:**
Same as BUG_002 — a broken sort control undermines a core shopping feature and gives users an inaccurate view of available pricing options.

---

## BUG_004 — Checkout form does not reliably accept typed text input

**Test Case Reference:** TC_030
**Module:** Checkout
**Environment:** Chrome browser, saucedemo.com, `problem_user` account
**Severity:** Critical
**Priority:** Critical

**Steps to Reproduce:**
1. Log in with `problem_user` / `secret_sauce`
2. Add a product to the cart and proceed to Checkout
3. Attempt to type into the First Name and Last Name fields

**Expected Result:**
Typed text should appear correctly in each field, allowing the user to complete checkout.

**Actual Result:**
Text entry is unreliable — in testing, the First Name field only registered a single character ("b") and the Last Name field remained empty despite input, blocking the checkout process from completing.

**Screenshot:** `Bugs_Screenshots/TC_030_bug.png`

**Impact:**
This is a blocking defect — if a real user experienced this, they would be unable to complete a purchase at all, resulting in direct lost sales.

---

## Summary

| Bug ID | Module | Severity | Status |
|---|---|---|---|
| BUG_001 | Inventory | Medium | Open |
| BUG_002 | Inventory | High | Open |
| BUG_003 | Inventory | High | Open |
| BUG_004 | Checkout | Critical | Open |

**Note:** All scenarios above were also tested using the `standard_user` account and passed without issue, confirming these defects are specific to the `problem_user` test account.
