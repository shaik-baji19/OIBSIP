# Task 10: Network Security Assessment Using Nmap and Wireshark

## 📌 Objective

The objective of this task was to perform a basic network security assessment by scanning a local Windows 11 system using **Nmap** and analyzing live network traffic using **Wireshark**. The assessment focused on identifying open ports, running services, network communication patterns, and recommending security improvements based on the findings.

---

## 🛠️ Tools Used

- Nmap 7.99
- Wireshark 4.6.6
- Windows 11
- Command Prompt (CMD)
- Google Chrome

---

## 🚀 Task Execution

### Step 1: Identify the Local System

The local system's IPv4 address was identified using the Windows Command Prompt.

```bash
ipconfig
```

**Observation**

The IPv4 address obtained from the system was used as the target for the Nmap scan.

---

### Step 2: Perform Network Scan Using Nmap

A service version detection scan was performed using the following command:

```bash
nmap -sV <YOUR_IP_ADDRESS>
```

The scan results were then saved using:

```bash
nmap -sV <YOUR_IP_ADDRESS> -oN nmap_results.txt
```

**Observation**

The scan successfully identified multiple open ports and the services running on the local system.

---

### Step 3: Capture Network Traffic

Wireshark was launched and the active **Wi-Fi** interface was selected for packet capture.

To generate traffic, multiple websites were visited using Google Chrome while Wireshark captured live packets.

**Observation**

Various protocols including **TCP**, **UDP**, **TLS**, **IPv6**, and **mDNS** were observed during packet capture.

---

### Step 4: Analyze Captured Packets

After sufficient traffic was captured, packet capture was stopped and saved as:

```text
wireshark_capture.pcap
```

The **TCP** display filter was applied to inspect only TCP packets.

**Observation**

Packet inspection revealed protocol layers including Ethernet, IPv6, and TCP, providing insight into how network communication occurs.

---

### Step 5: Security Assessment

The Nmap scan results and Wireshark packet capture were analyzed to identify potential security concerns and prepare a comprehensive network security assessment report.

---

## 📸 Screenshots

The screenshots demonstrating the task execution are available in the **screenshots/** directory.

The folder contains:

- `nmap_scan.png` – Nmap service version scan.
- `wireshark_capture.png` – Live packet capture using Wireshark.
- `tcp_filter.png` – TCP display filter applied in Wireshark.

---

## 📊 Assessment Summary

### Nmap Scan

The Nmap scan identified multiple open ports and active services running on the Windows 11 system.

Typical services observed included:

| Port | Service | Description |
|------|---------|-------------|
| 135 | MSRPC | Microsoft Remote Procedure Call |
| 139 | NetBIOS | Windows File and Printer Sharing |
| 445 | Microsoft-DS | SMB File Sharing |
| 2869 | HTTP | Microsoft HTTPAPI Service |
| 3306 | MySQL | MySQL Database Service |

---

### Wireshark Analysis

The captured network traffic contained several common networking protocols.

| Protocol | Description |
|----------|-------------|
| TCP | Reliable connection-oriented communication |
| UDP | Lightweight connectionless communication |
| TLS | Encrypted web communication |
| IPv6 | Internet Protocol Version 6 |
| mDNS | Local network service discovery |

---

## 🔍 Security Findings

The assessment identified the following observations:

- Multiple network services were accessible through open ports.
- File sharing services such as SMB and NetBIOS were active.
- Most web communication was encrypted using TLS.
- No suspicious or malicious traffic was observed during the packet capture.
- Open services should be periodically reviewed to reduce unnecessary network exposure.

---

## 🛡️ Security Recommendations

Based on the assessment, the following recommendations are suggested:

- Disable unused network services whenever possible.
- Restrict SMB and NetBIOS access to trusted systems only.
- Configure firewall rules to block unnecessary ports.
- Keep Windows and installed software updated.
- Monitor network traffic regularly.
- Perform periodic Nmap scans to identify newly exposed services.
- Use strong passwords and secure authentication.
- Conduct regular network security assessments.

---

## 📚 Learning Outcomes

Through this task, I learned how to:

- Perform a network security assessment.
- Identify open ports and active services using Nmap.
- Capture and analyze live network traffic using Wireshark.
- Apply protocol filters to inspect captured packets.
- Interpret network communication patterns.
- Identify potential security risks.
- Document technical findings in a professional assessment report.

---

## 📂 Repository Structure

```text
OIBSIP/
│
└── BajiShaik_Task10/
    │
    ├── README.md
    ├── network_security_assessment.md
    ├── nmap_results.txt
    ├── wireshark_capture.pcap
    │
    └── screenshots/
        ├── nmap_scan.png
        ├── wireshark_capture.png
        └── tcp_filter.png
```

---

## ✅ Conclusion

This task successfully demonstrated a basic network security assessment using **Nmap** and **Wireshark**. The assessment identified active network services, analyzed captured network traffic, and evaluated the system's security posture. Although no critical security issues were detected during the assessment, implementing appropriate security controls, monitoring network activity, and conducting regular assessments are essential for maintaining a secure network environment.

---

## 👨‍💻 Author

**Baji Shaik**

Security Analyst Intern

**Oasis Infobyte**
