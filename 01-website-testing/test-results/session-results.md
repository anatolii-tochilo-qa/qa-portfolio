# Session Management Test Results

## Executed Tests

| Test ID | Test Scenario | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| SESSION-001 | Open shopping cart immediately after login | Shopping cart opens and user remains authenticated | Shopping cart opened successfully; authentication was preserved | PASS |

## Observations

### OBS-003 — Unexpected Logout When Opening Shopping Cart

- **Environment:** Windows 10, Google Chrome 157.0.8103.38 (64-bit)
- **Time since login:** Approximately 15–30 minutes
- **Actual Result:** Application requested authentication again when navigating to the shopping cart
- **Reproducibility:** Not reproduced during immediate retry
- **Status:** Needs Investigation
- **Possible Cause:** Session expiration or session state issue (not confirmed)

## Planned Tests

- SESSION-002 — Verify session behavior after 20 minutes of inactivity (Not Run)
