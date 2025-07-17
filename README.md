# Cybersecurity Lab Projects

This repository documents vulnerability scans and penetration testing exercises performed in my cybersecurity homelab. Each project includes the tools used, commands, and why the scan or technique is important for real-world security testing.

---

## Basic Nmap Scan

This scan was performed against Metasploitable to identify open ports, running services, and potential vulnerabilities.

**Command used:**
```bash
nmap -sV -A <Metasploitable_IP>
```

The output is saved in [nmap_basic_scan.txt](./nmap_basic_scan.txt).

**Why this matters:**
- Helps enumerate services for further exploitation
- Identifies outdated software versions
- Provides OS and network info for deeper testing

---

## Nikto Web Vulnerability Scan

This scan checked for common web vulnerabilities and misconfigurations on the target's HTTP service.

**Command used:**
```bash
nikto -h http://<Metasploitable_IP>
```

The output is saved in [nikto_web_scan.txt](./nikto_web_scan.txt).

**Why this matters:**
- Quickly identifies outdated web servers
- Finds default files and weak configurations
- Useful for web application penetration testing

---


---

## Medusa SSH Brute Force Attempt

This test simulated a brute force attack against the Metasploitable SSH service using the **rockyou.txt** wordlist to try common passwords.

**Command used:**
\`\`\`bash
medusa -h 192.168.1.171 -u msfadmin -P /usr/share/wordlists/rockyou.txt -M ssh -t 4 -O medusa_ssh_results.txt
\`\`\`

The scan was **manually stopped** after a partial run. No valid password was discovered during this attempt.  

The partial results were saved in **medusa_ssh_results.txt**.

**Why this matters:**
- Demonstrates how attackers automate SSH brute-force attacks using common wordlists  
- Highlights the importance of strong, unique passwords and account lockout policies  
- Shows how detection systems can alert on repeated failed login attempts  

---

## Medusa SSH Brute Force Attempt

This test simulated a brute force attack against the Metasploitable SSH service using the **rockyou.txt** wordlist to try common passwords.

**Command used:**
\`\`\`bash
medusa -h 192.168.1.171 -u msfadmin -P /usr/share/wordlists/rockyou.txt -M ssh -t 4 -O medusa_ssh_results.txt
\`\`\`

The scan was **manually stopped** after a partial run. No valid password was discovered during this attempt.  

The partial results wer

