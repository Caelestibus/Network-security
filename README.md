# Network-security
Introduction to Network Security (Kali Linux Only)


**Internship Project @ Redynox**  
**Machine Used**: Kali Linux (Standalone)  
**26th**: June 2025

---

## 🧩 Objective

Understand the basics of network security by:

- Learning about common network threats
- Implementing basic firewall rules on Kali
- Using Wireshark to analyze network traffic
- Documenting key observations and learnings

---

## ⚠️ Network Threats Researched


| Threat Type        | Description |
|--------------------|-------------|
| **Virus**          | Malicious code that replicates by attaching itself to files. |
| **Worm**           | A standalone malware that spreads across networks automatically. |
| **Trojan Horse**   | Malware disguised as legitimate software. |
| **Phishing**       | Deceptive emails or sites to steal sensitive information. |
| **DoS/DDoS**       | Overwhelming a system to disrupt its availability. |
| **Man-in-the-Middle** | Intercepting communication between parties. |
| **Packet Sniffing**| Capturing data packets to analyze or steal sensitive info. |

---

## 🔧 Basic Security Measures on Kali


### ✅ UFW (Uncomplicated Firewall) Setup

```bash
sudo apt update && sudo apt install ufw -y
sudo ufw enable
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw status verbose
```

---

## 🔍 Explanation

Deny incoming – blocks unsolicited traffic from external sources

Allow outgoing – permits normal browsing and system updates

UFW status – verifies active rules and profiles

---


## 📶 Router Security Notes

Since I used a mobile hotspot, I couldn't access router settings like 192.168.1.1.

However, for secure Wi-Fi environments:

✅ Change the default admin password

✅ Use WPA2 or WPA3 encryption

---


## ❌ Disable WPS to prevent brute-force attacks

🔬 Wireshark Network Monitoring (on Kali)



🧪 Steps Followed:

- Installed Wireshark:

```bash
sudo apt install wireshark -y
sudo wireshark
```

---

- Chose interface: wlan0 or eth0

Applied filters:

- http
- dns
- tcp.port == 443


