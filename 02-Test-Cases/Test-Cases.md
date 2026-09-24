# TEST CASES - E-Commerce Application

## LOGIN MODULE (12 Test Cases)

| TC_ID | Module | Title | Precondition | Steps | Expected | Priority | Status |
|-------|--------|-------|---|---|---|---|---|
| TC_001 | Login | Valid credentials | App loaded | 1. Enter email 2. Enter password 3. Click login | User logged in | High | PASS |
| TC_002 | Login | Empty email | App loaded | 1. Leave email empty 2. Enter password 3. Click login | Error: "Email required" | High | FAIL |
| TC_003 | Login | Empty password | App loaded | 1. Enter email 2. Leave password empty 3. Click login | Error: "Password required" | High | FAIL |
| TC_004 | Login | Invalid email format | App loaded | 1. Enter "notanemail" 2. Enter password 3. Click login | Error: "Invalid email" | High | FAIL |
| TC_005 | Login | Wrong password | App loaded | 1. Enter valid email 2. Enter wrong password 3. Click login | Error: "Invalid credentials" | High | FAIL |
| TC_006 | Login | Password min 8 chars | App loaded | 1. Enter email 2. Enter 8-char password 3. Click login | User logged in | High | PASS |
| TC_007 | Login | Password below min (7) | App loaded | 1. Enter email 2. Enter 7-char password 3. Click login | Error: "Min 8 chars" | High | FAIL |
| TC_008 | Login | Password max 20 chars | App loaded | 1. Enter email 2. Enter 20-char password 3. Click login | User logged in | High | PASS |
| TC_009 | Login | Password above max (21) | App loaded | 1. Enter email 2. Enter 21-char password 3. Click login | Error: "Max 20 chars" | High | FAIL |
| TC_010 | Login | Case sensitivity | App loaded | 1. Enter EMAIL in CAPS 2. Enter password 3. Click login | Depends on system | Medium | PASS |
| TC_011 | Login | Spaces in credentials | App loaded | 1. Enter " email " 2. Enter " password " 3. Click login | Spaces trimmed | Medium | PASS |
| TC_012 | Login | Non-existent user | App loaded | 1. Enter fake@example.com 2. Enter password 3. Click login | Error: "Invalid credentials" | High | FAIL |

## SEARCH MODULE (10 Test Cases)

| TC_ID | Module | Title | Precondition | Steps | Expected | Priority | Status |
|-------|--------|-------|---|---|---|---|---|
| TC_013 | Search | Valid search term | Home page | 1. Enter "Laptop" 2. Click Search | Results displayed | High | PASS |
| TC_014 | Search | Empty search | Home page | 1. Leave empty 2. Click Search | Error or all products | High | FAIL |
| TC_015 | Search | Single character | Home page | 1. Enter "A" 2. Click Search | Results with "A" | Medium | PASS |
| TC_016 | Search | Special characters | Home page | 1. Enter "@#$%" 2. Click Search | Error or no results | Medium | FAIL |
| TC_017 | Search | Non-existent product | Home page | 1. Enter "xyz999" 2. Click Search | No products found | High | FAIL |
| TC_018 | Search | Long search (100 chars) | Home page | 1. Enter 100-char string 2. Click Search | Results or error | Medium | FAIL |
| TC_019 | Search | Case insensitive | Home page | 1. Search "laptop" then "LAPTOP" | Same results | Medium | PASS |
| TC_020 | Search | With spaces | Home page | 1. Enter " Laptop " 2. Click Search | Results (trimmed) | Low | PASS |
| TC_021 | Search | Price filter min | Home page | 1. Search + min $100 | Only ≥$100 | High | PASS |
| TC_022 | Search | Price filter max | Home page | 1. Search + max $1000 | Only ≤$1000 | High | PASS |

## SHOPPING CART (15 Test Cases)

| TC_ID | Module | Title | Precondition | Steps | Expected | Priority | Status |
|-------|--------|-------|---|---|---|---|---|
| TC_023 | Cart | Add 1 item | Product page | 1. Click "Add to Cart" qty 1 | Item added | High | PASS |
| TC_024 | Cart | Add qty 0 (invalid) | Product page | 1. Enter qty 0 2. Click Add | Error: "Qty ≥1" | High | FAIL |
| TC_025 | Cart | Add qty 1 (min) | Product page | 1. Enter qty 1 2. Click Add | Item added | High | PASS |
| TC_026 | Cart | Add qty 100 (max) | Product page | 1. Enter qty 100 2. Click Add | Item added | High | PASS |
| TC_027 | Cart | Add qty 101 (above max) | Product page | 1. Enter qty 101 2. Click Add | Error: "Max 100" | High | FAIL |
| TC_028 | Cart | Add qty -5 (negative) | Product page | 1. Enter qty -5 2. Click Add | Error: "Invalid" | Medium | FAIL |
| TC_029 | Cart | Add qty "abc" (text) | Product page | 1. Enter qty "abc" 2. Click Add | Error: "Must be number" | Medium | FAIL |
| TC_030 | Cart | Multiple items total | Cart page | 1. Add 2x$50 + 1x$30 | Total: $130 | High | PASS |
| TC_031 | Cart | Remove item | Cart page | 1. Add item 2. Click Remove | Item removed | High | PASS |
| TC_032 | Cart | Update quantity | Cart page | 1. Add item 2. Change qty to 5 | Cart recalculated | High | PASS |
| TC_033 | Cart | Apply 10% discount | Cart page | 1. Enter "SAVE10" 2. Apply | $100 → $90 | High | PASS |
| TC_034 | Cart | Invalid coupon | Cart page | 1. Enter "FAKE123" 2. Apply | Error: "Invalid" | High | FAIL |
| TC_035 | Cart | Expired coupon | Cart page | 1. Enter "EXPIRED" 2. Apply | Error: "Expired" | Medium | FAIL |
| TC_036 | Cart | Proceed to checkout | Cart page | 1. Add items 2. Click Checkout | Checkout page | High | PASS |
| TC_037 | Cart | Save for later | Cart page | 1. Add 2. Click "Save for later" | Item saved | Medium | PASS |

## CHECKOUT (15 Test Cases)

| TC_ID | Module | Title | Precondition | Steps | Expected | Priority | Status |
|-------|--------|-------|---|---|---|---|---|
| TC_038 | Checkout | Valid address | Checkout page | 1. Fill address 2. Continue | Accepted | High | PASS |
| TC_039 | Checkout | Empty address | Checkout page | 1. Leave empty 2. Continue | Error: "Required" | High | FAIL |
| TC_040 | Checkout | ZIP 4 digits (below min) | Checkout page | 1. Enter "1234" 2. Continue | Error: "Need 5" | High | FAIL |
| TC_041 | Checkout | ZIP 5 digits (valid) | Checkout page | 1. Enter "12345" 2. Continue | Accepted | High | PASS |
| TC_042 | Checkout | ZIP 6 digits (above max) | Checkout page | 1. Enter "123456" 2. Continue | Error: "Too long" | High | FAIL |
| TC_043 | Checkout | Phone 9 digits (below) | Checkout page | 1. Enter "123456789" 2. Continue | Error: "Need 10" | High | FAIL |
| TC_044 | Checkout | Phone 10 digits (valid) | Checkout page | 1. Enter "1234567890" 2. Continue | Accepted | High | PASS |
| TC_045 | Checkout | Phone 11 digits (above) | Checkout page | 1. Enter "12345678901" 2. Continue | Error: "Too long" | High | FAIL |
| TC_046 | Checkout | Select shipping | Checkout page | 1. Select "Standard" | Selected | High | PASS |
| TC_047 | Checkout | View summary | Review page | 1. Complete form 2. View | All items shown | High | PASS |
| TC_048 | Checkout | Apply promo | Checkout page | 1. Enter promo 2. Apply | Discount applied | High | PASS |
| TC_049 | Checkout | Select payment | Payment page | 1. Select Credit Card 2. Enter | Accepted | High | PASS |
| TC_050 | Checkout | Invalid card | Payment page | 1. Enter fake card 2. Submit | Error: "Invalid" | High | FAIL |
| TC_051 | Checkout | Process payment | Payment page | 1. Enter valid 2. Process | Submitted | High | PASS |
| TC_052 | Checkout | Order confirmation | Confirmation page | 1. Complete checkout 2. View | Order number shown | High | PASS |

## USER ACCOUNT (8 Test Cases)

| TC_ID | Module | Title | Precondition | Steps | Expected | Priority | Status |
|-------|--------|-------|---|---|---|---|---|
| TC_053 | Account | View profile | Account page | 1. Click Profile | User info displayed | High | PASS |
| TC_054 | Account | Edit profile | Account page | 1. Click Edit 2. Change name 3. Save | Changes saved | High | PASS |
| TC_055 | Account | View order history | Account page | 1. Click Orders | Past orders shown | High | PASS |
| TC_056 | Account | Track order | Account page | 1. Click order 2. Track | Tracking shown | High | PASS |
| TC_057 | Account | Save address | Account page | 1. Add address 2. Save | Address saved | Medium | PASS |
| TC_058 | Account | View wishlist | Account page | 1. Click Wishlist | Saved items shown | Medium | PASS |
| TC_059 | Account | Add to wishlist | Product page | 1. Click "Add to Wishlist" | Item saved | Medium | PASS |
| TC_060 | Account | Remove from wishlist | Account page | 1. Click Remove | Item removed | Low | PASS |

## MISC (5 Test Cases)

| TC_ID | Module | Title | Precondition | Steps | Expected | Priority | Status |
|-------|--------|-------|---|---|---|---|---|
| TC_061 | General | Home page load | Browser | 1. Navigate to app | Loads <3 seconds | Medium | PASS |
| TC_062 | General | Mobile responsive | Mobile view | 1. View on mobile | Layout adjusts | Medium | PASS |
| TC_063 | General | Browser compatibility | Firefox | 1. Test on Firefox | All features work | Medium | PASS |
| TC_064 | General | Logout | Logged in | 1. Click Logout | Logged out | High | PASS |
| TC_065 | General | Session timeout | Inactive | 1. Wait 30 mins inactive | Session expired | Medium | FAIL |

## TOTAL: 65+ TEST CASES

 BVA Examples Included (minimum 8 chars password, maximum 20 chars, etc.)
 ECP Examples Included (valid email format, invalid email format, etc.)
 Positive Testing (expected to pass)
 Negative Testing (expected to fail)
