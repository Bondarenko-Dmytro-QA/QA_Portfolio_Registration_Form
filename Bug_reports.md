# Bug Reports: User Registration Form

This document contains examples of bug reports that could be created during the testing of the registration form.

---
### BUG-001: System accepts a password without digits, violating the stated complexity requirements

**ID:** BR-REG-001
**Severity:** Major
**Priority:** High
**Environment:** `Windows 10, Chrome 108`

**Steps to Reproduce:**
1.  Navigate to the registration page.
2.  Fill out all required fields with valid data.
3.  In the "Password" and "Confirm Password" fields, enter a value that contains only letters (e.g., "Passwordtest").
4.  Click the "Register" button.

**Actual Result:**
The user is successfully registered, and an account is created.

**Expected Result:**
The registration should fail. An error message should appear under the "Password" field, indicating that the password does not meet the complexity requirements (e.g., "Password must contain at least one digit.").

---
### BUG-002: Email validation error message overlaps the "Phone" input field on mobile devices

**ID:** BR-REG-002
**Severity:** Minor
**Priority:** Medium
**Environment:** `Android 12, Chrome Mobile, Viewport 360x740px`

**Steps to Reproduce:**
1.  Open the registration page on a mobile device or using a mobile emulator in DevTools.
2.  Enter an invalidly formatted email (e.g., "test").
3.  Tap on any other field on the form to trigger the validation check.

**Actual Result:**
The error message "Invalid email format" appears and partially covers the "Phone" input field, making it difficult for the user to see and interact with it.

**Expected Result:**
The error message should be displayed correctly below the "Email" field without overlapping or obstructing any other form elements.

_Attachment: screenshot demonstrating the UI overlap._
