# Checklist: User Registration Form

This checklist provides a high-level overview of the test ideas and areas to be covered during the testing of the user registration form.

### ✅ Positive Scenarios (Happy Path)
- [ ] Successful registration using only the required valid data.
- [ ] Successful registration using all fields, including the optional "Patronymic" field.

### ❌ Negative Scenarios (Validation & Error Handling)
- [ ] **Required Fields:** Attempt to submit the form with each required field left empty, one by one.
- [ ] **Required Fields:** Attempt to submit the form with all required fields empty.
- [ ] **Uniqueness:** Attempt to register with an email that already exists in the system.
- [ ] **Uniqueness:** Attempt to register with a phone number that already exists.
- [ ] **Email Field Validation:**
    - [ ] Enter an email without the "@" symbol.
    - [ ] Enter an email without a domain part (e.g., `test@`).
    - [ ] Enter an email with special characters.
- [ ] **Phone Field Validation:**
    - [ ] Enter letters instead of digits.
    - [ ] Enter fewer digits than required.
    - [ ] Enter more digits than allowed.
- [ ] **Password Fields Validation:**
    - [ ] Enter a password that is shorter than the minimum length requirement.
    - [ ] Enter a password and a different confirmation password.
- [ ] **Name Fields Validation:**
    - [ ] Enter numbers or special characters in "First Name" and "Last Name" fields.

### 🎨 UI/UX Testing
- [ ] **Layout:** Verify that the form layout matches the design mockups (alignment, spacing, fonts, colors).
- [ ] **Placeholders:** Check that all input fields have correct and helpful placeholder text.
- [ ] **Error Messages:** Ensure that validation error messages are clear, user-friendly, and displayed in the correct location.
- [ ] **Responsiveness:** Verify that the form adapts correctly to different screen sizes, especially mobile viewports.

### 🔒 Basic Security Checks
- [ ] **Password Masking:** Confirm that characters entered in the "Password" and "Confirm Password" fields are masked (displayed as dots or asterisks).
- [ ] **Basic XSS:** Attempt to input a simple HTML/script tag (e.g., `<script>alert('test')</script>`) into text fields to ensure it is not executed.
