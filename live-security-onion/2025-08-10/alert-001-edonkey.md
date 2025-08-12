# Alert: eDonkey Traffic (ET P2P eDonkey Publicize File ACK)

**Date:** 2025-08-10  
**Severity:** Medium  
**Source:** Security Onion (Suricata)

## Summary
Detected potential eDonkey (P2P) traffic consistent with a “publicize file” ACK.

## Details
- **Rule/SID:** 2003311
- **Source IP:** <fill>
- **Destination IP:** <fill>
- **Proto/Port:** UDP/<fill>

## Analysis
Likely P2P behavior from a streaming app/device. Note policy and risk.

## Action
- Logged and monitored.
- Block or remove app if not allowed.

## Evidence
![eDonkey](artifacts/screenshots/edonkey.png)  
Raw export: `alerts-2025-08-10.csv`
