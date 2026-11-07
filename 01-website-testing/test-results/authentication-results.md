# Authentication Testing — Execution Results

## 1. Test Environment

| Parameter | Value |
|---|---|
| Application | SauceDemo |
| Operating System | Windows 10 |
| Browser | Google Chrome 157.0.8103.38 (x64) |
| Testing Type | Manual Testing |
| Test Module | Authentication |

## 2. Test Execution Results

| Test ID | Test Scenario | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| AUTH-001 | Login with standard_user | Successful login | Successful login | PASS |
| AUTH-006 | Login with locked_out_user | Access denied with lockout message | Lockout message displayed | PASS |
| AUTH-007 | Login with non-existing username | Authentication error | Username and password do not match any user in this service | PASS |
| AUTH-008 | Login with incorrect password | Authentication error | Username and password do not match any user in this service | PASS |
| AUTH-009 | Login with empty username | Username is required | Username is required | PASS |
| AUTH-010 | Existing username with empty password | Password is required | Password is required | PASS |
| AUTH-011 | Non-existing username with empty password | Password is required | Password is required | PASS |
| AUTH-012 | Login with admin:admin | Authentication error | Username and password do not match any user in this service | PASS |
| AUTH-013 | Both fields empty | Username is required | Username is required | PASS |
| AUTH-014 | Username containing spaces only | Authentication must be rejected | Username and password do not match any user in this service | OBSERVATION |
| AUTH-015 | Logout from standard user account | User is redirected to login page | User was redirected to login page | PASS |
| AUTH-016 | Access protected page after logout | Access denied for logged-out user | Access denied with authentication error | PASS |

## 3. Observations

### OBS-001 — Whitespace-only username

**Description:**

When entering whitespace characters in the Username field, the application does not display the "Username is required" validation message.

Instead, it displays:

`Epic sadface: Username and password do not match any user in this service`

**Actual behavior:**

The application treats the whitespace-only input as a non-empty value during authentication.

**Additional investigation:**

Further testing is required to determine whether whitespace trimming is part of the expected application behavior.

## 4. Execution Summary

- Executed test scenarios: 10
- Passed: 9
- Observations requiring clarification: 1
- Failed: 0

## 5. Conclusion

The initial authentication testing demonstrated that the application correctly handles standard login scenarios, invalid credentials, locked-out users and empty required fields.

One additional observation related to whitespace-only input was documented for further investigation.

**Testing Status:** In Progress
