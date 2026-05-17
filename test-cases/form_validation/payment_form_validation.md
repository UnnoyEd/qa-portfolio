# Payment Form – Test Cases

## Preconditions:
- User is on Payment Form page
- Form contains:
  - Card Number field
  - Safety Code (CVV) field
  - Save button
  - Back button
  
 ---
 
## Card Number Field - Validation
 
### TC-01 - Valid card and CVV numbers
 
**Steps:**
 1. Enter valid card number: 123456789012 (minimum allowed length)
 2. Enter valid CVV number
 3. Click "Save"
 
**Expected Result:**
Form is submitted successfully.
Success message is displayed.
 
---

### TC-02 - Card number with letters

**Steps:**
1. Enter card number: 4111abcd1111
2. Enter valid CVV
3. Click "Save"

**Expected Result:**
Validation error is displayed.

---

### TC-03 - Card number below minimum length

**Steps:**
1. Enter card number: 12345678901
2. Enter valid CVV
3. Click "Save"

**Expected Result:**
Validation error is displayed.

---

### TC-04 - Card number above maximum length

**Steps:**
1. Enter card number: 12345678901234567890
2. Enter valid CVV
3. Click "Save"

**Expected Result:**
Validation error is displayed.

---

### TC-05 - Card number formatted with spaces 

**Steps:**
1. Enter card number: 1234 5678 9012 3456
2. Enter valid CVV
3. Click "Save"

**Expected Result:**
Spaces are trimmed and card is processed successfully.

---
## CVV Field - Validation

### TC-06 - CVV number with letters

**Steps:**
1. Enter valid card number
2. Enter CVV number: 12a
3. Click "Save"

**Expected Result:**
Validation error is displayed.

---

### TC-07 - CVV number below minimum length

**Steps:**
1. Enter valid card number
2. Enter CVV number: 12
3. Click "Save"

**Expected Result:**
Validation error is displayed.

---

### TC-08 - CVV number above maximum length

**Steps:**
1. Enter valid card number
2. Enter CVV number: 1234
3. Click "Save"

**Expected Result:**
Validation error is displayed.

---

### TC-09 - Empty field handling

**Steps:**
1. Leave Card field empty
2. Leave CVV field empty
3. Click "Save"

**Expected Result:**
Form is not submitted.
Validation messages are displayed for required fields.

---

## Form Submission – Save Button Behavior

### TC-10 - Save button is active when input is valid

**Steps:**
1. Enter valid card number
2. Enter valid CVV number

**Expected Result:**
Save button is active.

### TC-11 - Save button is inactive when inputs are invalid

**Steps:**
1. Enter card number: 1234
2. Enter CVV number: 555555

**Expected Result:**
Save button is inactive.

---

## Navigation – Back Button Behavior

### TC-12 - Back button behavior

**Steps:**
1. Enter any card number
2. Enter any CVV number
3. Click "Back"
4. Click on the form again

**Expected Result:**
User is redirected to the previous page.
Unsaved data is not preserved.
