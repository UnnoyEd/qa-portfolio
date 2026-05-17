# Payment Form - Bug Reports

## Environment
- Application: Yandex Taxi frontend demo (QA training environment)
- Environment: Test
- Browser: Mozilla Firefox 140.0.2
- OS: Windows 10

## Global Preconditions
- User is on the Payment Form page
- Form is fully loaded and accessible
- All fields and buttons are visible
- All fields are cleared

---

## BR-001 - Validation error is not displayed when Card Number input includes disallowed symbols

**Related Test Case:** TC-02 – Card number with letters

**Issue:** System accepts invalid input without showing validation message.

**Reproduction Steps:**
1. Enter card number: 4111abcd1111
2. Enter valid CVV
3. Click "Save"

**Expected Result:**
Validation error is displayed.

**Actual Result:**
No validation error is displayed

**Severity:**
Medium

---

## BR-002 - Validation error is not displayed when card number is longer than maximum allowed length

**Related Test Case:** TC-04 – Card number above maximum length

**Issue:** System accepts invalid input without showing validation message.

**Reproduction Steps:**
1. Enter card number: 12345678901234567890
2. Enter valid CVV
3. Click "Save"

**Expected Result:**
Validation error is displayed.

**Actual Result:**
No validation error is displayed

**Severity:**
Medium

---

## BR-003 - Save button is active when CVV input is invalid

**Related Test Case:** TC-11 - Save button is inactive when inputs are invalid

**Issue:** Save button is active when inputs are invalid

**Reproduction Steps:**
1. Enter valid card number
2. Enter CVV number: 12
3. Click "Save"

**Expected Result:**
Save button is not active

**Actual Result:**
Save button is active

**Severity:**
High
