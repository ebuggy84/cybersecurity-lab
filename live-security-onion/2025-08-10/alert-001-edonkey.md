# ET P2P eDonkey Publicize File ACK

**Date/Time (ET):** <fill>  
**Rule/SID:** 2003311  
**Severity:** High  
**Module:** Suricata  

## What Triggered
Detected small UDP ACK consistent with eDonkey P2P “publicize file” behavior.

## Quick Triage
- Internal Host: Firestick (192.168.1.xxx)
- External IP: <fill>
- Likely from a streaming app using P2P.

## Action Taken
- Logged alert for tracking
- Consider blocking P2P traffic if against policy

## Evidence
- Screenshot: `artifacts/screenshots/edonkey.png`
- JSON event: `alerts-<DATE>.jsonl`
