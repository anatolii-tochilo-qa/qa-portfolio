# Session Management Test Results

## Executed Tests

| Test ID | Test Scenario | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| SESSION-001 | Open shopping cart immediately after login | Shopping cart opens and user remains authenticated | Shopping cart opened successfully; authentication was preserved | PASS |

## Observations

### OBS-003 — Unexpected Logout When Opening Shopping Cart

- **Reproducibility:** Observed twice during exploratory testing
- **First occurrence:** Approximately 15–30 minutes after login
- **Second occurrence:** Approximately 10 minutes after starting SESSION-002, while testing shopping cart functionality
- **Status:** Needs Investigation
- **Possible Cause:** Session expiration or session state issue (not confirmed)

## Planned Tests

- SESSION-002 — Verify session behavior after 20 minutes of inactivity (Not Run)
