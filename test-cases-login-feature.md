# Test Cases for the Login Feature

Gherkin language has been chosen to create these test cases It is a domain-specific language designed to write test cases in a clear and human-readable format. It uses simple keywords such as Given, When, Then, And, and But to define the context, action, and expected outcomes of a test scenario. This structured approach ensures that requirements and test cases are easy to understand for both technical and non-technical stakeholders.

During test execution, a test case can have different statuses based on its outcome:

  - Passed: The test case met all the expected outcomes successfully.
  - Failed: The test case did not meet the expected outcomes due to a defect or error.
  - Blocked: The test case could not be executed because of an unresolved dependency or issue.
  - Skipped: The test case was intentionally not executed, often due to conditions such as unimplemented functionality.
  - In Progress: The test case is currently being executed.

In addition to assigning a status, the actual result observed during test execution can also be recorded. This helps in documenting whether the system's behavior aligns with the expected results.

### Login - Test Cases

### TC001: Validate UI elements on login page

**Objective:** Verify that all UI elements of the login page are displayed correctly, including the logo, form placement, and labels.

**Preconditions:** The user should be redirected to the Login/Register page.

**Expected Results:** 

  - The logo is displayed on the left side of the page.
  - The login form is centered on the page.
  - The form contains the following elements:
    - Title: "Login on your account"
    - Subtitle: "Don’t you have an account? Create an account"
    - Username input field.
    - Password input field.
    - Login button.

**Steps:**

**Given** the user was redirected to the Login/Register page

**When** the user is on the Login page

**Then** the Logo will be available on the left side

**And** the form to Login will be available on the center of the page

**And** the form contains the title: "Login on your account"

**And** the form contains the subtitle: "Don’t you have an account? Create an account"

**And** the form contains a Username input

**And** the form contains a Password input

**And** the form contains a Login button

### TC002: Validate input field restrictions on login form

**Objective:** Ensure that the username and password fields enforce their respective input restrictions.

**Preconditions:** The user should be on the Login/Register page.

**Expected Results:**

  - The username field allows only alphabetical characters.
  - The password field allows letters, numbers, and special characters.

**Steps:**

**Given** the user is on the Login/Register page

**When** the user is filling the form

**Then** the Username field should allow only letters

**And** the Password field should allow numbers, letters and special characters 

### TC003: Error message for invalid login attempts

**Objective:** Verify that appropriate error messages are displayed when login attempts are made with invalid credentials.

**Preconditions:** The user should be on the Login/Register page.

**Expected Results:** 

  - For each invalid credentials scenario (wrong username/password combinations), a red error message appears below the password field.
  - The error message: "Sorry, your username or password are not correct. Please, try again."

**Steps:**

**Given** the user is on the Login/Register page

**When** the user tries to log in with < Invalid Credentials >

**And** the user clicks on the Login button

**Then** a red error message should appear below the Password field

**And** the message should say: "Sorry, your username or password are not correct. Please, try again."

|          Invalid Credentials           |
|----------------------------------------|
|  Wrong Username  and  Wrong password   |
|  Wrong Username  and  Correct password |
|  Correct Username  and  Wrong password |

### TC004: Verify successful login and redirection

**Objective:** Validate that logging in with correct credentials redirects the user to the correct page and displays a success message.

**Preconditions:** The user should be on the Login/Register page with valid credentials.

**Expected Results:**

  - Upon clicking the login button with valid credentials, the user is redirected to the My Expenses Table page.
  - A success message appears, stating: "You are logged in."

**Steps:**

**Given** the user is on the Login/Register page

**When** the user clicks on the Login button with valid credentials

**Then** the user should be redirected to the Home page

**And** a message saying: "You are logged in." should appear
