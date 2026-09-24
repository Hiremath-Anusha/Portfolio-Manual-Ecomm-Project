# Test Execution Report

**Date:** 10.07.2026
**Tester:** Anusha Hiremath
**Application:** Sauce Labs Demo
**Testing Duration:** 10 days

## Executive Summary

| Metric | Value |
|--------|-------|
| **Total Test Cases** | 65 |
| **Passed** | 54 |
| **Failed** | 9 |
| **Blocked** | 2 |
| **Pass Rate** | 83.1% |
| **Defects Found** | 11 |

## Test Coverage by Module

| Module | Test Cases | Passed | Failed | Coverage |
|--------|-----------|--------|--------|----------|
| Login | 12 | 10 | 2 | 83% |
| Search | 10 | 8 | 2 | 80% |
| Cart | 15 | 13 | 2 | 87% |
| Checkout | 15 | 14 | 1 | 93% |
| Account | 8 | 8 | 0 | 100% |
| Misc | 5 | 1 | 2 | 20% |
| **TOTAL** | **65** | **54** | **9** | **83.1%** |

## Defects Summary

### Critical (Severity: CRITICAL)
1. Login button unresponsive on Firefox

### High Priority (Severity: HIGH)
1. Cart calculation error with discount
2. Search filter fails with special characters
3. Payment gateway timeout

### Medium Priority (Severity: MEDIUM)
1. Mobile UI alignment issue
2. Loading spinner missing on checkout
3. Sort by price inconsistent
4. Profile update data not saved
5. Wishlist not persisting after logout

### Low Priority (Severity: LOW)
1. Minor typo in terms page
2. Button color slightly off on hover

## Key Findings

1. **Critical Issue:** Firefox compatibility problem with login button - needs immediate attention
2. **High Priority:** Cart calculation logic error with discount codes - affects revenue
3. **High Priority:** Search functionality broken with special characters - limits user experience
4. **Recommendation:** Fix critical and high-priority bugs before production release

## Quality Assessment

Overall application quality: GOOD
- 83.1% pass rate indicates stable core functionality
- Critical issues must be resolved
- High-priority bugs should be fixed for better user experience
- Application ready for UAT after bug fixes

## Recommendations

1. **Immediate Action:** Fix critical Firefox compatibility issue
2. **Priority 1:** Resolve cart calculation logic for discount codes
3. **Priority 2:** Fix search filter special character handling
4. **Priority 3:** Address payment gateway timeout
5. **Future:** Implement automated regression tests

## Conclusion

Testing completed with 65 test cases across 6 core modules. 
11 defects identified and documented.
83.1% pass rate shows application is mostly functional.
Ready for UAT after critical and high-priority bug fixes.

---
**Report Status:** Complete
**Date:** 10.07.2026

