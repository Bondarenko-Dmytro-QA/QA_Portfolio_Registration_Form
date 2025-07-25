# Test Cases: User Registration Form

This document provides detailed, step-by-step test cases for the key scenarios of the user registration functionality.

---
### **ID:** TC-REG-001
**Title:** Successful registration using valid required data
**Priority:** High

**Preconditions:**
*   The user is on the registration page.
*   The email and phone number to be used are unique and not yet registered in the system.

**Steps:**
1.  Enter a valid value in the "First Name" field (e.g., "Dmytro").
2.  Enter a valid value in the "Last Name" field (e.g., "Bondarenko").
3.  Enter a unique, validly formatted email in the "Email" field.
4.  Enter a unique, validly formatted phone number in the "Phone" field.
5.  Enter a password that meets the complexity requirements in the "Password" field.
6.  Enter the same password in the "Confirm Password" field.
7.  Click the "Register" button.

**Expected Result:**
1.  The system successfully creates a new user account.
2.  A success message (e.g., "Registration successful!") is displayed to the user.
3.  The user is redirected to the login page or their new personal account dashboard.

---
### **ID:** TC-REG-002
**Title:** Attempt to register using an email that already exists in the system
**Priority:** High

**Preconditions:**
*   The user is on the registration page.
*   The email `test@example.com` is already associated with an existing account.

**Steps:**
1.  Fill in all fields with otherwise valid data.
2.  In the "Email" field, enter `test@example.com`.
3.  Click the "Register" button.

**Expected Result:**
1.  The registration process fails.
2.  A clear and user-friendly error message is displayed directly under the "Email" field, such as "A user with this email already exists."
3.  All other data entered by the user in the form remains intact.
