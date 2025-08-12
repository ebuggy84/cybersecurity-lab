# Alert: HTTP Client Body contains `otp=` in cleartext

**Date:** 2025-08-10  
**Severity:** High  
**Source:** Security Onion (Suricata)

## Summary
HTTP request body included `otp=` over cleartext HTTP.

## Details
- **Rule/SID:** 2035090
- **Source IP:** <fill>
- **Destination IP:** <fill>
- **Proto/Port:** HTTP/80

## Analysis
OTP/credentials should not be sent over HTTP. Possible insecure flow.

## Action
- Identify source app/user.
- Enforce HTTPS for auth endpoints.
- Check if any creds/OTP were exposed.

## Evidence
![HTTP OTP](artifacts/screenshots/http-otp.png)  
Raw export: `alerts-2025-08-10.csv`
