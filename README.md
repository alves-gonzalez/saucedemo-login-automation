🧪 Saucedemo Login Test (Cypress)

This repository contains a personal automated end-to-end test project built with Cypress for validating the login functionality on Saucedemo.com
. The test ensures that users with valid credentials can successfully sign in and reach the inventory page.

📋 Test Overview

Test Name: Suacedemo Login - Positive Test
Purpose: Verify that a valid user can log in successfully.
Framework: Cypress.io

Language: JavaScript (ES6)
Test File: saucedemo_login.cy.js

🧠 Test Scenario
TC001 - Login with Valid Credentials

Preconditions:

User credentials are stored in fixtures/users.json.

Test Steps:

Navigate to the Saucedemo login page.

Enter a valid username.

Enter a valid password.

Click the Login button.

Verify the page redirects to inventory.html.

Assert that the Products title is visible.

Expected Result:
The user should be successfully redirected to the Inventory page, and the "Products" heading should be displayed.
