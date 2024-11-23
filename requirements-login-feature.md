# Requirements for the Login Feature

These requirements were created to serve as examples. Each requirement specifies functionalities and behaviors that a login feature must fulfill. Based on these requirements, the test cases can be developed to validate the UI layout, input field behavior, error handling, and authentication processes, ensuring the system functions as intended.

### UI Requirements:

**Page Layout**

- The page must have a logo displayed on the left side.
- A Login form must be centered on the page.

**Form Titles and Labels**

- The form must display a title: "Login on your account."
- The form must display a subtitle: "Don’t you have an account? Create an account."

**Input Fields**

The Login form must include:
  - A Username input field.
  - A Password input field.

**Action Button**

  - The form must include a Login button to submit credentials.

### Input Fields Validation Requirements:

**Input Validation**

  - The Username field must only allow alphabetic characters.
  - The Password field must accept a combination of numbers, letters, and special characters.

### Error Handling Requirements:

**Invalid Login Attempt Behavior**

  - The system must display an error message when detecting invalid login attempts using the following scenarios:
    - Both Username and Password are incorrect.
    - Username is incorrect but Password is correct.
    - Username is correct but Password is incorrect.

  - When an invalid login attempt occurs:
    - A red error message must be displayed below the Password field.
    - The error message text must be: "Sorry, your username or password are not correct. Please, try again."

### Authentication and Navigation Requirements:

**Successful Login Behavior**

  - The system must verify user credentials (Username and Password).
  - When the credentials are valid:
    - The user must be redirected to the My Expenses Table page.
    - A confirmation message must appear on the page: "You are logged in."
