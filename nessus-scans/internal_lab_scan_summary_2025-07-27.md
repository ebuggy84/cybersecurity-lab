# Internal Vulnerability Scan Summary (2025-07-27)

## Overview
- **Scan Type:** Basic Network Scan  
- **Scope:** Entire internal network *(limited to 16 hosts by Nessus Essentials)*  
- **Total Vulnerabilities Found:** *368*  
- **Top Affected Hosts:**
  - `192.168.1.1` → 126 vulnerabilities (10 Medium, 116 Info)
  - `192.168.1.80` → 68 vulnerabilities
  - `192.168.1.67` → 61 vulnerabilities
  - `192.168.1.84` → 42 vulnerabilities
  - *(additional hosts detected, but capped by Nessus Essentials)*

## Severity Breakdown
- **Critical:** *0*
- **High:** *0*
- **Medium:** *Approx 20+*
- **Low/Info:** *Majority informational findings*

## Most Common Vulnerabilities
1. **Outdated Apache / Web services** → Potential remote code execution  
2. **Weak SSH/Telnet configurations** → Easier brute-force attacks  
3. **Exposed SMB shares with old protocols** → Lateral movement risks  
4. **Missing security patches on multiple hosts** → Exploitable known CVEs  

## SOC-Style Recommendations
- ✅ **Patch & update critical services** (Apache, SSH, SMB)  
- ✅ **Apply OS & firmware updates** on network devices  
- ✅ **Harden SSH/Telnet access** – enforce key-based auth or disable legacy protocols  
- ✅ **Implement network segmentation** for high-value assets  
- ✅ **Re-run scans after remediation** to confirm risk reduction  

> **Note:** This scan only covered **16 hosts due to Nessus Essentials licensing.**  
> More hosts are likely vulnerable. Consider upgrading Nessus or segmenting scans.

---

### Files in this Folder
- `internal_lab_scan_2025-07-27.nessus` → Raw Nessus scan results  
- `internal_lab_scan_summary_2025-07-27.md` → This summary  

