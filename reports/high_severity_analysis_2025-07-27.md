# High Severity Alert Analysis – 2025-07-27

This report summarizes **high severity alerts** captured from Security Onion on **July 27, 2025**.  
The data comes from the CSV export `alerts/high_severity_alerts_2025-07-27.csv`.

---

## 📊 Alert Summary
- **Total Alerts Captured:** 513  
- **Source:** Suricata IDS/IPS  
- **Severity:** High only  

---

## 🔥 Top Alert Categories
1. **Log4j RCE Attempt (CVE-2021-44228)**  
   - Multiple inbound & outbound LDAP attempts
2. **Apache Struts OGNL Injection (CVE-2017-5638)**  
   - Remote Code Execution attempts via crafted URIs
3. **Cross-Site Scripting (XSS) Tags in URI**  
   - Possible reconnaissance for web vulnerabilities
4. **SSH Brute Force Attempts**  
   - Failed login attempts targeting internal hosts
5. **Suspicious P2P / Gnutella Connections**  
   - Potential unwanted traffic or malware beaconing

---

## 🕵️ Notable Patterns
- **Multiple Exploit Variants for Log4j**  
  - Different transport layers (LDAP, UDP, TCP bypass techniques)
- **Outbound Traffic Detected**  
  - Some alerts show outbound LDAP queries, suggesting possible compromise
- **Web Exploit Attempts**  
  - Apache & NodeJS exploit attempts, likely automated scanners

---

## ✅ Recommended Actions
1. **Review impacted hosts** for possible exploitation  
2. **Check outbound LDAP traffic** – ensure no compromised systems  
3. **Apply/verify patches** for Apache Struts, Log4j, NodeJS  
4. **Hunt for related IOCs** in other logs  
5. **Consider blocking malicious IPs** detected during these attempts  

---

## 📂 Files in this report
- `alerts/high_severity_alerts_2025-07-27.csv` – raw CSV export of all high severity alerts  
- `reports/high_severity_analysis_2025-07-27.md` – this analysis  

---

*Generated as part of the Security Onion SOC Lab project.*
