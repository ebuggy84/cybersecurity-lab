# ET INFO HTTP Client Body contains otp= in cleartext

**Date/Time (ET):** <fill>  
**Rule/SID:** 2035090  
**Severity:** High  
**Module:** Suricata  

## What Triggered
Detected HTTP traffic with `otp=` parameter in cleartext body.

## Quick Triage
- Internal Host: <fill>
- External IP: <fill>
- Possible insecure credential/token transmission.

## Action Taken
- Logged alert for tracking
- Investigate if OTP was legitimate or malicious

## Evidence
- Screenshot: `artifacts/screenshots/http-otp.png`
- JSON event: `alerts-<DATE>.jsonl`
