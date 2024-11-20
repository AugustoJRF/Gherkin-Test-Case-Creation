# Test Cases for the Login Feature

### Login - Test Cases

### TC001: Validate UI elements on login page

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

**Given** the user is on the Login/Register page

**When** the user is filling the form

**Then** the Username field should allow only letters

**And** the Password field should allow numbers, letters and special characters 

### TC003: Error message for invalid login attempts

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

**Given** the user is on the Login/Register page

**When** the user clicks on the Login button with valid credentials

**Then** the user should be redirected to the My expenses table page

**And** a message saying: "You are logged in." should appear
