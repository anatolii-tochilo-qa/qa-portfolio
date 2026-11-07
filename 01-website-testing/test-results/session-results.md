# Session Management Test Results

## Executed Tests

| Test ID | Test Scenario | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| SESSION-001 | Open shopping cart immediately after login | Shopping cart opens and user remains authenticated | Shopping cart opened successfully; authentication was preserved | PASS |
| SESSION-002 | Verify session after 12 minutes of inactivity | Session behavior follows the defined timeout requirements | After 12 minutes of inactivity, navigation triggered a redirect to the login page; no automatic redirect occurred while idle | NEEDS INVESTIGATION |

## Observations

### OBS-003 — Unexpected Logout During Shopping Cart Testing

- **Environment:** Windows 10, Chrome 157.0.8103.38 (64-bit)
- **Occurrences:** 2
- **Time since login:** Approximately 10 minutes (not confirmed)
- **Actual Result:** User was redirected to the login page.
- **Error Message:** Epic sadface: You can only access '/inventory.html' when you are logged in.
- **Reproducibility:** Observed twice during exploratory testing.
- **Status:** Needs Investigation
- **Possible Cause:** Session expiration or session state issue (not confirmed).
- **Browser Tabs:** One SauceDemo tab
- **First Occurrence:** Unexpected logout when navigating to the shopping cart
- **Second Occurrence:** Unexpected logout when navigating from the shopping cart to the product catalog
- **Session Duration:** Approximately 10 minutes (unconfirmed)

