# Daily Security Onion Alert Summary — 2025-08-10

## Alerts logged
1. eDonkey P2P ACK (SID 2003311) — Medium  
2. HTTP OTP in cleartext (SID 2035090) — High  
3. SOC Login Failure (UUID bf86ef21...) — Medium

## Notes
- OTP over HTTP is highest risk; enforce HTTPS.
- eDonkey likely P2P from a streaming device; review policy.
- Login failures: confirm if user error vs brute force.

## Evidence
- Screenshots in `artifacts/screenshots/`
- CSV export: `alerts-2025-08-10.csv`
