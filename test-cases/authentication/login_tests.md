# Login Functionality – Test Cases

## Preconditions:
- Application is accessible and running
- User is on the login page:
    https://kittygram-frontend-1.prakticum-team.ru/signin
- Test user account exists:
	  login: engelskeLetter 
	  password: ktokto17
 
---

## TC-001 – Successful login with valid credentials

### Steps:
1. Enter valid username: engelskeLetter
2. Enter valid password: ktokto17
3. Click “Login”

### Expected Result:
User is successfully authenticated and redirected to the dashboard.

---

## TC-002 – Login with invalid password

### Steps:
1. Enter valid username: engelskeLetter 
2. Enter incorrect password
3. Click “Login”

### Expected Result:
User is not authenticated.
An error message is displayed indicating invalid credentials.

---

## TC-003 – Login with invalid username

### Steps:
1. Enter invalid username
2. Enter any password
3. Click “Login”

### Expected Result:
User is not authenticated.
An error message is displayed indicating invalid credentials.

---

## TC-004 – Login with empty fields

### Steps:
1. Leave username empty
2. Leave password empty
3. Click “Login”

### Expected Result:
User is not authenticated.
Validation messages are shown for required fields.

---

## TC-005 – Login with only username filled

### Steps:
1. Enter valid username: engelskeLetter
2. Leave password empty
3. Click “Login”

### Expected Result:
System prompts user to fill in the password field.

---

## TC-006 – Login with only password filled

### Steps:
1. Leave username empty
2. Enter password
3. Click “Login”

### Expected Result:
System prompts user to fill in the username field.

---

## TC-007 – Login with leading/trailing spaces in credentials

### Steps:
1. Enter valid username with spaces (" engelskeLetter ")
2. Enter valid password with spaces (" ktokto17 ")
3. Click “Login”

### Expected Result:
According to requirements, login attempt is rejected when credentials contain leading or trailing spaces.
User is not authenticated and an error message is displayed.

---

## TC-008 – Login with special characters injection attempt

### Steps:
1. Enter `' OR 1=1 --` as username
2. Enter any password
3. Click “Login”

### Expected Result:
System does not allow authentication bypass.
User is not authenticated.
Authentication error is displayed.

---

## TC-009 – Password field masking verification

### Steps:
1. Enter any password in password field

### Expected Result:
Password characters are masked (e.g. ●●●●●).

---

## TC-010 – Error message validation

### Steps:
1. Attempt login with invalid credentials

### Expected Result:
User is not authenticated.
An error message "Invalid login or password" is displayed.
