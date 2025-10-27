🧪 Saucedemo Cypress E2E Login Tests

This repository contains end-to-end tests built with Cypress to validate the login functionality of Saucedemo.com

The tests verify both positive and negative login scenarios, ensuring that authentication, logout, and user flow behave as expected.

🧰 Tech Stack

Testing Framework: Cypress.io

Language: JavaScript (ES6)

Assertion Library: Chai (built into Cypress)

Helper Library: @testing-library/cypress

Test Type: Functional / UI End-to-End

📁 Project Structure
📦 saucedemo-login-test-cypress
 ┣ 📂 cypress
 ┃ ┣ 📂 e2e
 ┃ ┃ ┣ 📜 saucedemo_login_positive.cy.js
 ┃ ┃ ┗ 📜 saucedemo_login_negative.cy.js
 ┃ ┣ 📂 fixtures
 ┃ ┃ ┗ 📜 users.json
 ┣ 📜 cypress.config.js
 ┣ 📜 package.json
 ┗ 📜 README.md

🧪 Test Suite Overview
TC001 - Login and Logout with Valid Credentials (Positive Test)

Goal:
Verify that a valid user can successfully log in and log out.

Steps:

Navigate to the login page.

Enter a valid username and password from users.json.

Click the Login button.

Verify that the browser redirects to inventory.html.

Assert that the Products page title is visible.

Open the hamburger menu and click Logout.

Verify the user is redirected back to the login page and the Login button is visible.

Expected Result:
User is successfully logged in, can access the inventory page, and can log out returning to the login page.

TC002 - Invalid Login Attempt (Negative Test)

Goal:
Verify that the application correctly displays an error message when invalid credentials are used.

Steps:

Navigate to the login page.

Enter an invalid username and password from users.json.

Click the Login button.

Verify the error message:

Epic sadface: Sorry, this user has been locked out.


Expected Result:
The error message should be displayed, and the user should not be able to access the inventory page.

📄 Sample users.json
{
  "validUser": {
    "username": "standard_user",
    "password": "secret_sauce"
  },
  "invalidUser": {
    "username": "locked_out_user",
    "password": "secret_sauce"
  }
}

⚙️ Setup Instructions
1. Clone the Repository
git clone https://github.com/<your-username>/saucedemo-login-test-cypress.git
cd saucedemo-login-test-cypress

2. Install Dependencies
npm install

3. Open Cypress Test Runner
npx cypress open

4. Run Tests Headlessly
npx cypress run

🧾 Test Execution Logs

When run successfully, Cypress output should show:

✔ TC001 - Login in with valid credentials (passed)
✔ TC002 - Log in with invalid credentials (passed)


Both tests log custom Cypress messages like:

Login Successful

Logout Successful

Invalid login error message verified

📈 Future Enhancements

Add test cases for locked user, empty field validation, and performance assertions.

Include screenshot/video reports using Cypress reporters.

Integrate with CI/CD pipelines (GitHub Actions or Jenkins).

👨‍💻 Author

Alves Gonzalez
🔗 GitHub

🔗 LinkedIn
