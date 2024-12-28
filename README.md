# Insecure User Data Access in Express.js Route
This repository demonstrates a common vulnerability in Express.js applications: insecure access to user data due to improper input validation in route parameters.  The bug allows unauthorized access to user information by manipulating the route parameter.

## Vulnerability
The `/users/:id` route directly uses the `req.params.id` value to query the database.  If the `id` is not properly sanitized or validated, an attacker could potentially use SQL injection or other techniques to access unintended data.

## Solution
The solution involves adding input validation to ensure the `id` is a valid number before querying the database.  This prevents malicious input from compromising the application's security.