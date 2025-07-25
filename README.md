# 🛡️ Security Onion Network Monitoring & Threat Detection  

This project demonstrates **live network monitoring and threat detection** using **Security Onion** in a homelab environment. It captures real network traffic, detects suspicious behavior using **Suricata IDS/IPS**, and generates actionable alerts for SOC-style analysis.  

---

## ✅ Project Overview  

- **Platform:** Security Onion (Suricata, Elasticsearch, Kibana, TheHive)  
- **Purpose:** Simulate a SOC environment to detect, investigate, and document real network alerts  
- **Focus Areas:**  
  - IDS/IPS rule-based alerting  
  - Detecting suspicious domains, DNS queries, and SSH brute-force attempts  
  - Creating SOC-style reports for incident handling  

---

## 🏗️ Lab Architecture  

- **Security Onion** deployed for live network monitoring  
- **Suricata** for deep packet inspection & alert generation  
- **Kibana & TheHive** for SOC-style analysis and case management  
- **Simulated traffic** from test machines to trigger real alerts  

---

## 🖧 Network Architecture  

Below is the network architecture used in this lab, showing how traffic is monitored by Security Onion through a network tap:  

![Network Architecture](https://raw.githubusercontent.com/ebuggy84/security-onion-network-monitoring/main/network-diagram.png)

- **ISP → Modem → Tap → UDM Pro**  
- **Tap → Security Onion (monitoring live traffic)**  
- **UDM Pro → Aggregation Switch → Lab & Home Network Devices**  

This setup ensures full packet visibility while isolating monitoring from production traffic.  

---

## 🚨 High & Medium Alerts  

Here are **real alerts** captured in this lab environment:  

| **Timestamp** | **Alert Title** | **Severity** | **Source** |  
|---------------|-----------------|--------------|------------|  
| 2025-07-24 11:54:46 | Security Onion - Grid Node Login Failure (SSH) | **High** | Suricata |  
| 2025-07-24 07:34:59 | ET INFO Http Client Body contains pwd= in cleartext | **High** | Suricata |  
| 2025-07-23 22:13:10 | GPL ATTACK_RESPONSE id check returned root | **High** | Suricata |  
| 2025-07-23 22:12:56 | GPL ATTACK_RESPONSE id check returned root | **High** | Suricata |  
| 2025-07-23 22:11:41 | GPL ATTACK_RESPONSE id check returned root | **High** | Suricata |  

---

## 📊 SOC-Style Analysis  

- **SSH Login Failure:** Detected multiple failed login attempts on Security Onion node, indicating a possible brute-force attack.  
- **Cleartext Password Detected:** HTTP traffic containing `pwd=` keyword in the body, a sign of insecure credential transmission.  
- **Privilege Escalation Response:** The `id check returned root` alert suggests a post-exploitation phase where an attacker gained root-level privileges.  

---

## 🔧 Tools Used  

- **Suricata IDS/IPS** → Captures & analyzes packets  
- **Kibana** → Visualizes logs & alerts  
- **TheHive** → Case management & incident tracking  
- **ElasticSearch** → Stores and indexes alert data  

---

## 📌 Next Steps  

- Expand detection rules for additional TTPs (MITRE ATT&CK mapping)  
- Automate alert forwarding to TheHive for case creation  
- Integrate Cortex analyzers for deeper threat intelligence  

---

### ✉️ Contact  

If you’re interested in my work or want to collaborate on security projects, feel free to connect!  

---


