# BUG REPORTS - E-Commerce Testing

## Bug #001

**Title:** Login button unresponsive on Firefox

**Severity:** 🔴 CRITICAL

**Priority:** HIGH

**Status:** Open

**Environment:** Firefox, Windows 10

**Steps to Reproduce:**
1. Open app in Firefox
2. Enter email: standard_user
3. Enter password: password123
4. Click "Sign In" button

**Expected Result:**
User is logged in and dashboard is displayed

**Actual Result:**
Login button doesn't respond. Page freezes.

---

## Bug #002

**Title:** Cart calculation error with discount

**Severity:** 🟠 HIGH

**Priority:** HIGH

**Status:** Open

**Environment:** Chrome, Windows 10

**Steps to Reproduce:**
1. Add item: $100
2. Apply coupon: SAVE10 (10% discount)
3. View cart total

**Expected Result:**
Total should be $90 (100 - 10%)

**Actual Result:**
Total shows $100 (discount not applied)

---

## Bug #003

**Title:** Search filter fails with special characters

**Severity:** 🟠 HIGH

**Priority:** HIGH

**Status:** Open

**Environment:** Chrome, Windows 10

**Steps to Reproduce:**
1. Enter search: "@#$%"
2. Click Search button
3. View results

**Expected Result:**
Error message or no results

**Actual Result:**
Page crashes

---

## Bug #004

**Title:** Payment gateway timeout error

**Severity:** 🟠 HIGH

**Priority:** HIGH

**Status:** Open

**Environment:** Chrome, Windows 10

**Steps to Reproduce:**
1. Complete checkout form
2. Click "Process Payment"
3. Wait for confirmation

**Expected Result:**
Payment processed in 5-10 seconds

**Actual Result:**
Error: "Gateway timeout" after 30 seconds

---

## Bug #005

**Title:** Mobile UI alignment issue

**Severity:** 🟡 MEDIUM

**Priority:** MEDIUM

**Status:** Open

**Environment:** Mobile, Chrome

**Steps to Reproduce:**
1. Open app on mobile (375px width)
2. Navigate to checkout
3. View address form

**Expected Result:**
Form fields properly aligned

**Actual Result:**
Form fields overflow screen

---

## Bug #006

**Title:** Loading spinner missing on checkout

**Severity:** 🟡 MEDIUM

**Priority:** MEDIUM

**Status:** Open

**Environment:** Chrome, Windows 10

**Steps to Reproduce:**
1. Click "Proceed to Checkout"
2. Observe page loading

**Expected Result:**
Loading spinner shown while page loads

**Actual Result:**
No loading indicator; appears frozen

---

## Bug #007

**Title:** Sort by price inconsistent

**Severity:** 🟡 MEDIUM

**Priority:** MEDIUM

**Status:** Open

**Environment:** Chrome, Windows 10

**Steps to Reproduce:**
1. Click "Sort by Price (Low to High)"
2. View product list
3. Click "Sort by Price (High to Low)"
4. View product list

**Expected Result:**
Results sorted correctly both ways

**Actual Result:**
Sorting inconsistent on second click

---

## Bug #008

**Title:** Profile update data not saved

**Severity:** 🟡 MEDIUM

**Priority:** MEDIUM

**Status:** Open

**Environment:** Chrome, Windows 10

**Steps to Reproduce:**
1. Go to Account page
2. Click Edit Profile
3. Change name to "Test User"
4. Click Save
5. Refresh page

**Expected Result:**
New name persists after refresh

**Actual Result:**
Name reverted to original

---

## Bug #009

**Title:** Wishlist not persisting after logout

**Severity:** 🟡 MEDIUM

**Priority:** MEDIUM

**Status:** Open

**Environment:** Chrome, Windows 11 Pro

**Steps to Reproduce:**
1. Add item to Wishlist
2. Click Logout
3. Log back in
4. View Wishlist

**Expected Result:**
Added item still in wishlist

**Actual Result:**
Wishlist is empty

---

## Bug #010

**Title:** Minor typo in terms page

**Severity:** 🟢 LOW

**Priority:** LOW

**Status:** Open

**Environment:** Chrome, Windows 10

**Steps to Reproduce:**
1. Go to Terms & Conditions page
2. Read paragraph 3

**Expected Result:**
No spelling errors

**Actual Result:**
Word "teh" instead of "the"

---

## Bug #011

**Title:** Button color slightly off on hover

**Severity:** 🟢 LOW

**Priority:** LOW

**Status:** Open

**Environment:** Chrome, Windows 10

**Steps to Reproduce:**
1. Hover over "Add to Cart" button
2. Observe color change

**Expected Result:**
Button color changes to specified shade

**Actual Result:**
Button color slightly different shade

---

**TOTAL BUGS: 11**
- Critical: 1
- High: 3
- Medium: 5
- Low: 2
