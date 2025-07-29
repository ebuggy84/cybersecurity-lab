## Nessus Scan - Before Remediation

This screenshot shows the vulnerabilities discovered in the initial scan before any patches or updates were applied.

![Nessus Scan](nessus_before_remediation_2025-07-27.png)

## Nessus Scan - Before Remediation (192.168.1.1)

This scan targeted the UDM Pro Max on the home network. It uncovered multiple low-to-medium risk findings. All findings were reviewed for relevance and remediation options. Since the device functions as the main gateway, several items were expected behavior.

![Nessus Scan](nessus_before_remediation_2025-07-27.png)

### Key Findings:

**1. IP Forwarding Enabled**  
Expected for a router handling network traffic. No action taken.

**2. SSL (Multiple Issues)**  
Modern UniFi OS enforces HTTPS by default. Legacy SSL toggles are deprecated and not user-configurable.

**3. HTTP (Multiple Issues)**  
HTTP traffic successfully redirects to HTTPS. No sensitive data served via HTTP. Port 80 remains open for redirect. Optional firewall rule not applied at this time.

**4. DHCP Server Detection**  
The UDM Pro Max is actively managing DHCP, as intended.

**5. ICMP Timestamp Disclosure**  
No available UI or CLI method to disable this on UniFi OS. Risk is low and mitigation is not currently implemented.

---

```markdown
### ✅ Apache2 Remediation – After Fixes

This screenshot confirms the successful remediation of the Apache2-related findings identified during the initial scan. A new scan was conducted after implementing fixes to reduce the reported vulnerabilities.

#### 🔧 Remediation Actions Taken:

1. **Apache2 Version Updated**  
   The outdated Apache2 web server was upgraded to the latest version.

   ```bash
   sudo apt update
   sudo apt upgrade apache2 -y
   ```

2. **Unnecessary Modules Removed**  
   Disabled modules that were not required and could expose additional attack surfaces.

   ```bash
   sudo a2dismod autoindex status info
   sudo systemctl restart apache2
   ```

3. **Cleaned Default Web Root**  
   Removed unnecessary files and sample content from the default Apache directory.

   ```bash
   sudo rm -rf /var/www/html/index.html
   ```

4. **Tightened File Permissions**  
   Ensured proper ownership and permission settings to protect web files.

   ```bash
   sudo chown -R www-data:www-data /var/www
   sudo chmod -R 755 /var/www
   ```

5. **Suppressed Server Information**  
   Prevented Apache from disclosing version and OS info in responses.  
   Edited `/etc/apache2/conf-available/security.conf` and set:

   ```apache
   ServerTokens Prod
   ServerSignature Off
   ```
```
