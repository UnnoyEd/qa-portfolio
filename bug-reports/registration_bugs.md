# Registration Functionality - Bug Reports

## Environment
- Application: Kittygram frontend demo (QA training environment)
- Environment: Test 
- Browser: Mozilla Firefox 140.0.2
- OS: Windows 10

## Global Preconditions
- User is on the Sign Up page
- Form is fully loaded and ready for interaction
- Test user account exists:
	- login: engelskeLetter 
	- password: ktokto17

---

## BR-001 - Registration is allowed with password shorter than 8 characters

**Related Test Case:** TC-004 – Sign up with password shorter than 8 characters

**Issue:** System allows registration with a password shorter than the minimum allowed length (8 characters)

**Reproduction Steps:**
1. Enter any username
2. Enter any e-mail
3. Enter a short password: 3ab
4. Click “Sign up”

**Expected Result:**
User is not registered.
Validation message is shown prompting the user to create longer password.

**Actual Result:**
User is registered successfully.

**Severity:**
High

---

## BR-002 - Registration is allowed with username longer than 40 characters

**Related Test Case:** TC-006 – Sign up with a long username

**Issue:** System allows registration with username longer than the maximum allowed length (40 characters)

**Reproduction Steps:**
1. Enter any username longer than 40 characters
2. Enter any e-mail
3. Enter any password
4. Click “Sign up”

**Expected Result:**
User is not registered.
Validation message is shown indicating username length restrictions.

**Actual Result:**
User is registered successfully.

**Severity:**
High

---

## BR-003 - Registration is allowed with registered e-mail

**Related Test Case:** TC-010 – Sign up with an existing e-mail

**Issue:** System allows registration of duplicate accounts

**Reproduction Steps:**
1. Successfully register an account
2. Return to the sign up page
3. Enter any username
4. Enter previously used e-mail
5. Enter any password
6. Click "Sign up"

**Expected Result:**
User is not registered.
Validation message is shown indicating that this account already exists.

**Actual Result:**
User is registered successfully.

**Severity:**
High

