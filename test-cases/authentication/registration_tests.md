# Sign up Functionality – Test Cases

## Preconditions:
- Application is accessible and running
- User is on the sign up page:
	https://kittygram-frontend-1.prakticum-team.ru/signup
 
---

## TC-001 – Successful registration with valid data

### Steps:
1. Enter valid username: TestUser852
2. Enter valid e-mail: test@gmail.com
3. Enter valid password: 123456ab
4. Click “Sign up”

### Expected Result:
User is successfully registered and redirected to the login page.

---

## TC-002 – Sign up with empty fields

### Steps:
1. Leave username empty
2. Leave e-mail empty
3. Leave password empty
4. Click “Sign up”

### Expected Result:
User is not registered.
Validation messages are shown for required fields.

---

## TC-003 – Sign up with incorrect e-mail format

### Steps:
1. Enter valid username
2. Enter e-mail without the @
3. Enter valid password
4. Click “Sign up”

### Expected Result:
User is not registered.
An error message is displayed indicating invalid e-mail format.

---

## TC-004 – Sign up with password shorter than 8 characters

### Steps:
1. Enter any username
2. Enter any e-mail
3. Enter a short password: 3ab
4. Click “Sign up”

### Expected Result:
User is not registered.
Validation message is shown prompting the user to create longer password.

---

## TC-005 – Sign up with password containing only numbers

### Steps:
1. Enter any username
2. Enter any e-mail
3. Enter password containing only numbers: 123456789
4. Click “Sign up”

### Expected Result:
User is not registered.
Validation message is displayed according to password requirements.

---

## TC-006 – Sign up with a long username

### Steps:
1. Enter any username longer than 40 characters
2. Enter any e-mail
3. Enter any password
4. Click “Sign up”

### Expected Result:
User is not registered.
Validation message is shown indicating username length restrictions.

---

## TC-007 – Sign up with white spaces before and after the values

### Steps:
1. Enter any valid username with spaces (" testrest ")
2. Enter any valid e-mail with spaces (" test@test.com ")
3. Enter any valid password with spaces (" ktokto17 ")
4. Click “Sign up”

### Expected Result:
Leading/trailing spaces are trimmed.
User is registered successfully and redirected to the login page.

---

## TC-008 – Sign up with special characters injection attempt

### Steps:
1. Enter `' OR 1=1 --` as username
2. Enter any e-mail.
3. Enter any password
4. Click “Sign up”

### Expected Result:
User is not registered.
Validation message is displayed indicating that the input is not allowed.

---

## TC-009 – Sign up with an existing username

### Steps:
1. Register an account
2. Return to the sign up page
3. Enter the previously used username
4. Enter any e-mail
5. Enter any password
6. Click "Sign up"

### Expected Result:
User is not registered.
Validation message is shown indicating that the username is taken.

---

## TC-010 – Sign up with an existing e-mail

### Steps:
1. Return to the sign up page
2. Enter any username
3. Enter previously used e-mail
4. Enter any password
5. Click "Sign up"

### Expected Result:
User is not registered.
Validation message is shown indicating that this account already exists.
