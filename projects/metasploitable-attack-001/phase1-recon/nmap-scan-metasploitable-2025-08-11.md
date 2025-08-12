# Nmap Scan - Metasploitable

**Date:** 2025-08-11  
**Target:** 192.168.1.59  
**Command Used:**
```bash
nmap -sV -p- 192.168.1.59 -oN nmap_full.txt
```

---

## Scan Results

**Host:** metasploitable.localdomain  
**MAC Address:** BC:24:11:07:8B:BA (Proxmox Server Solutions GmbH)  
**OS:** Unix, Linux  
**CPE:** cpe:/o:linux:linux_kernel

---

### Open Ports and Services

| Port | State | Service | Version |
|------|-------|---------|---------|
| 21/tcp | open | ftp | vsftpd 2.3.4 |
| 22/tcp | open | ssh | OpenSSH 4.7p1 Debian 8ubuntu1 (protocol 2.0) |
| 23/tcp | open | telnet | Linux telnetd |
| 25/tcp | open | smtp | Postfix smtpd |
| 53/tcp | open | domain | ISC BIND 9.4.2 |
| 80/tcp | open | http | Apache httpd 2.2.8 ((Ubuntu) DAV/2) |
| 111/tcp | open | rpcbind | 2 (RPC #100000) |
| 139/tcp | open | netbios-ssn | Samba smbd 3.X - 4.X (workgroup: WORKGROUP) |
| 445/tcp | open | netbios-ssn | Samba smbd 3.X - 4.X (workgroup: WORKGROUP) |
| 512/tcp | open | exec | netkit-rsh rexecd |
| 513/tcp | open | login | Linux login service |
| 514/tcp | open | shell | Metasploitable root shell |
| 1099/tcp | open | java-rmi | GNU Classpath grmiregistry |
| 1524/tcp | open | bindshell | Metasploitable root shell |
| 2049/tcp | open | nfs | 2-4 (RPC #100003) |
| 2121/tcp | open | ftp | ProFTPD 1.3.1 |
| 3306/tcp | open | mysql | MySQL 5.0.51a-3ubuntu5 |
| 3632/tcp | open | distccd | GNU 4.2.4 (Ubuntu 4.2.4-1ubuntu4) |
| 5432/tcp | open | postgresql | PostgreSQL DB 8.3.0 - 8.3.7 |
| 5900/tcp | open | vnc | VNC (protocol 3.3) |
| 6000/tcp | open | X11 | access denied |
| 6667/tcp | open | irc | UnrealIRCd |
| 6697/tcp | open | irc | UnrealIRCd |
| 8009/tcp | open | ajp13 | Apache Jserv (Protocol v1.3) |
| 8180/tcp | open | http | Apache Tomcat/Coyote JSP engine 1.1 |
| 8787/tcp | open | drb | Ruby DRb RMI (Ruby 1.8; path /usr/lib/ruby/1.8/drb) |
| 9100/tcp | open | jetdirect | HP Jetdirect printer server |
| 49152/tcp | open | rpc | 1 (RPC #100024) |
| 49153/tcp | open | rpc | 1 (RPC #100021) |

---

### Notes:
- Many services are outdated and vulnerable by design for practice purposes.
- This scan is the **initial reconnaissance** stage in our attack chain.
- Next steps will involve targeted enumeration against specific services such as SMB, FTP, HTTP, and databases.

---

**File Generated:** `nmap-scan-metasploitable-2025-08-11.md`  
**Purpose:** Store and track scan results for vulnerability testing and exploitation in later steps.
