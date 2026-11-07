# Session Management Test Results

## Executed Tests

| Test ID | Test Scenario | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| SESSION-001 | Open shopping cart immediately after login | Shopping cart opens and user remains authenticated | Shopping cart opened successfully; authentication was preserved | PASS |
| SESSION-002 | Verify session after 12 minutes of inactivity | Session behavior follows the defined timeout requirements | After 12 minutes of inactivity, navigation triggered a redirect to the login page; no automatic redirect occurred while idle | NEEDS INVESTIGATION |
| SESSION-003 | Verify session persistence during regular navigation | Session behavior follows the defined timeout requirements | Session expired after 10 minutes despite regular navigation between pages | NEEDS INVESTIGATION |

## Observations

### OBS-003 — Session Expiration During Navigation

- **Environment:** Windows 10, Chrome 157.0.8103.38 (64-bit)
- **Browser Tabs:** One SauceDemo tab
- **Actual Result:** After the session expired, navigating to another page redirected the user to the login page.
- **Error Message:** `Epic sadface: You can only access '/inventory.html' when you are logged in.`
- **First Occurrence:** Redirect occurred when navigating to the shopping cart.
- **Second Occurrence:** Redirect occurred when navigating from the shopping cart to the product catalog.
- **SESSION-002 Result:** After 12 minutes of inactivity, navigation triggered a redirect to the login page. No automatic redirect occurred while idle.
- **SESSION-003 Result:** Session expired after 10 minutes despite regular navigation between pages.
- **Hypothesis:** Possible absolute session timeout independent of user activity.
- **Reproducibility:** Reproduced during controlled testing.
- **Status:** Reproduced — Requirements Not Confirmed.
