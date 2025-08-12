# Alert: Security Onion — SOC Login Failure

**Date:** 2025-08-10  
**Severity:** Medium  
**Source:** Security Onion (Sigma)

## Summary
Failed login detected on the SOC web UI.

## Details
- **Rule UUID:** bf86ef21-41e6-417b-9a05-b9ea6bf28a38
- **Source IP:** <fill>
- **User/Account:** <fill>
- **Attempts/Window:** <fill>

## Analysis
Could be user error or brute force. Correlate with auth logs.

## Action
- Verify account activity.
- If malicious, block source and enforce MFA/lockout.

## Evidence
![SOC Login Fail](artifacts/screenshots/soc-login-fail.png)  
Raw export: `alerts-2025-08-10.csv`
