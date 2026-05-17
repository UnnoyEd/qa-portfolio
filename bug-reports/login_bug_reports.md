# Login Functionality - Bug Reports

## Environment
- Application: Kittygram frontend demo (QA training environment)
- Environment: Test / Staging
- Browser: Mozilla Firefox 140.0.2
- OS: Windows 10

## Global Preconditions
- User is on the Login page
- Form is fully loaded and ready for interaction
- Test user account exists:
	- login: engelskeLetter 
	- password: ktokto17

---

## BR-001 - Login is allowed with empty password

**Related Test Case:** TC-005 – Login with only username filled

**Issue:** User is authenticated without providing password.

**Reproduction Steps:**
1. Enter username: engelskeLetter
2. Leave password empty
3. Click "Login"

**Expected Result:**
User is not authenticated.
System prompts user to fill in the password field.

**Actual Result:**
User is authenticated successfully

**Severity:**
High

---

## BR-002 - Login is allowed with trailing spaces after login and password

**Related Test Case:** TC-007 – Login with leading/trailing spaces in credentials

**Issue:** User is logged in with trailing spaces after login and password

**Reproduction Steps:**
1. Enter valid username with trailing spaces ("engelskeLetter ")
2. Enter valid password with trailing spaces ("ktokto17 ")
3. Click "Login"

**Expected Result:**
Login attempt is rejected.
User is not authenticated.
Validation error is displayed.

**Actual Result:**
User is logged in.

**Severity:**
High
