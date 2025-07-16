# cybersecurity-lab
Documenting my cybersecurity homelab projects, vulnerability scans, penetration testing, and SOC workflows.
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
