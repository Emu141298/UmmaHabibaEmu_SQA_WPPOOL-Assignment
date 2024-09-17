WordPress Automation Tests for WP Dark Mode Plugin
This repository contains Cypress-based automated test cases for testing the WP Dark Mode Plugin on a WordPress installation. These tests cover plugin installation, activation, customization, and frontend verification. The tests ensure that the WP Dark Mode plugin is functioning correctly on the WordPress site by automating essential workflows like enabling dark mode, customizing switch styles, and validating accessibility settings.

Prerequisites
Before running the tests, ensure the following dependencies and setup are in place:

Local Environment:
WordPress installed on a local server (XAMPP, WAMP, MAMP, or Local by Flywheel).
WooCommerce plugin (optional).
WP Dark Mode Plugin (tested plugin).
Node.js and npm installed on your machine.
Tools & Libraries:
Cypress is used for automating the test cases.
Setup Instructions
1. Clone the Repository:
bash
Copy code
git clone https://github.com/yourusername/wp-dark-mode-automation.git
cd wp-dark-mode-automation
2. Install Cypress:
Make sure you have Node.js installed, then install Cypress by running the following command:

bash
Copy code
npm install cypress --save-dev
3. Configure WordPress Credentials:
You need to update the test script (cypress/integration/wp-dark-mode-tests.spec.js) with your WordPress credentials and site URL:

WordPress Username: Add your WordPress admin username.
WordPress Password: Add your WordPress admin password.
WordPress URL: Replace 'http://localhost/wordpress/wp-login.php' with your local WordPress URL if it's different.
Example in the test:

javascript
Copy code
cy.visit('http://localhost/wordpress/wp-login.php');
cy.get('#user_login').type('YOUR_USERNAME');
cy.get('#user_pass').type('YOUR_PASSWORD');
4. Running the Tests:
Once everything is configured, you can run the Cypress tests using:

bash
Copy code
npx cypress open
This will open the Cypress Test Runner, where you can run the test suite for WP Dark Mode.

Alternatively, you can run tests headlessly with:

bash
Copy code
npx cypress run
Test Coverage
1. WordPress Admin Login:
Verifies if the admin can log in successfully.
2. WP Dark Mode Plugin Installation & Activation:
Checks if the WP Dark Mode Plugin is active, installs it if not, and activates it.
3. Enable Admin Dashboard Dark Mode:
Automates the process of enabling dark mode for the WordPress admin dashboard.
4. Change Floating Switch Style:
Changes the floating switch style to validate customization.
5. Customize Switch Size and Position:
Changes the size and position of the floating switch on the frontend.
6. Disable Keyboard Shortcuts (Accessibility):
Disables the keyboard shortcuts from the plugin’s accessibility settings.
7. Enable Page-Transition Animations:
Enables page transition animations for better frontend user experience.
8. Validate Frontend Dark Mode Functionality:
Verifies if dark mode is working correctly on the frontend.
Issue Tracking and Suggestions
During the preparation of the automation test suite, any bugs, suggestions, or feature requests can be tracked using GitHub Issues. To ensure efficient issue management, custom labels are created for priority and severity.

Custom Labels:
Priority:
P1 (High Priority): Blockers or major issues that stop test execution.
P2 (Medium Priority): Non-blocking issues that should be fixed but allow tests to continue.
P3 (Low Priority): Minor issues or suggestions that do not significantly affect test execution.
Severity:
Critical: Bugs that make the system unusable or affect essential functionality.
Major: Significant bugs that affect a large portion of the user experience but are not critical.
Minor: Small UI bugs or minor issues that don’t impact core functionality.
Issues can be raised in the same repository to keep track of test-related problems and communicate them to developers efficiently.

Screenshots & Reports
The test suite automatically captures screenshots at critical points, such as:

After plugin activation.
When dark mode is enabled in the admin dashboard.
After modifying switch styles and frontend validation.


BUG, Screen record attached here in the repository
