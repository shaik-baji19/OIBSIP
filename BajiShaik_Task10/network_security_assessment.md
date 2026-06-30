# Network Security Assessment Report

## Task Information

**Task Name:** Network Security Assessment

**Internship:** Oasis Infobyte Security Analyst Internship

**Tools Used:** Nmap, Wireshark, Windows Command Prompt, Google Chrome

---

# 1. Introduction

The purpose of this network security assessment was to evaluate the security posture of a local Windows 11 system using Nmap and Wireshark. The assessment focused on identifying open ports, running services, and analyzing captured network traffic to understand communication patterns and identify potential security risks.

Network security assessments help identify exposed services, improve network visibility, and strengthen overall system security by detecting potential vulnerabilities before they can be exploited.

---

# 2. Objectives

The primary objectives of this assessment were:

* Identify open ports and active network services.
* Capture live network traffic.
* Analyze communication between the local system and external networks.
* Identify potential security vulnerabilities.
* Recommend security improvements based on the findings.

---

# 3. Tools Used

| Tool | Purpose |
|------|---------|
| Nmap | Network discovery and port scanning |
| Wireshark | Network traffic capture and analysis |
| Windows Command Prompt | Executing Nmap scan commands |
| Google Chrome | Generating network traffic for analysis |

---

# 4. Methodology

## Step 1: Network Identification

The local system's IPv4 address was identified using the following command:

```bash
ipconfig
```

The detected IPv4 address was used as the target for the Nmap scan.

---

## Step 2: Network Scanning with Nmap

The following command was executed:

```bash
nmap -sV <YOUR_IP_ADDRESS> -oN nmap_results.txt
```

### Purpose

* Identify open ports.
* Detect running services.
* Perform service version detection.
* Save the scan results for documentation.

The scan results were saved as:

```text
nmap_results.txt
```

---

## Step 3: Traffic Capture Using Wireshark

Wireshark was used to capture live network traffic while browsing websites using Google Chrome.

Activities included:

* Visiting multiple websites
* HTTPS communication
* General web browsing

The captured traffic was saved as:

```text
wireshark_capture.pcap
```

---

# 5. Findings

## Nmap Scan Results

The Nmap scan identified several open ports and running services on the local Windows system.

Example services observed:

| Port | Service | Description |
|------|---------|-------------|
| 135 | MSRPC | Microsoft Remote Procedure Call |
| 139 | NetBIOS | Windows File and Printer Sharing |
| 445 | Microsoft-DS | SMB File Sharing |
| 2869 | HTTP | Microsoft HTTPAPI Service |
| 3306 | MySQL | MySQL Database Service |

### Observations

* Multiple Windows services were accessible through open ports.
* File sharing and remote communication services were active.
* Open ports should be monitored and secured to minimize potential attack surfaces.

---

## Wireshark Traffic Analysis

The captured network traffic contained multiple protocols generated during normal web browsing.

### Protocols Observed

* TCP
* UDP
* TLS
* IPv6
* mDNS

### Observations

* TCP packets represented reliable communication between systems.
* TLS traffic indicated encrypted web communication.
* UDP packets supported lightweight network communication.
* IPv6 packets showed modern IP addressing in use.
* mDNS packets were used for local network device discovery.

---

# 6. Vulnerability Analysis

## Vulnerability 1: Open Network Services

### Description

Open ports expose network services that may become targets for unauthorized access if left unsecured.

### Risk Level

Medium

### Impact

Attackers may attempt to exploit exposed services if proper security controls are not implemented.

---

## Vulnerability 2: File Sharing Services

### Description

SMB and NetBIOS services are commonly used for Windows file sharing and should only be accessible to trusted systems.

### Risk Level

Medium

### Impact

Improperly configured file sharing services may expose sensitive resources.

---

## Vulnerability 3: Network Service Exposure

### Description

Running unnecessary services increases the system's attack surface.

### Risk Level

Low to Medium

### Impact

Unused services provide additional opportunities for attackers to identify potential weaknesses.

---

# 7. Risk Assessment

| Finding | Risk Level |
|----------|------------|
| Open Network Ports | Medium |
| SMB and NetBIOS Services | Medium |
| Service Exposure | Medium |
| Encrypted TLS Traffic | Low |
| IPv6 Communication | Low |

---

# 8. Security Recommendations

The following recommendations are suggested to improve network security:

1. Disable unused network services whenever possible.
2. Restrict SMB and NetBIOS access to trusted systems.
3. Configure firewall rules to limit unnecessary open ports.
4. Keep Windows and all installed software updated.
5. Monitor network traffic regularly using Wireshark.
6. Perform periodic Nmap scans to detect newly exposed services.
7. Use strong passwords and secure authentication methods.
8. Enable encryption for sensitive network communications.
9. Review system logs for suspicious activity.
10. Conduct regular network security assessments.

---

# 9. Conclusion

The network security assessment successfully identified active network services and analyzed network traffic using Nmap and Wireshark. The assessment demonstrated how network scanning and packet analysis can be used to understand system exposure and monitor communication across the network.

Although no critical security issues were observed during this assessment, implementing the recommended security measures will help reduce potential risks and improve the overall security posture of the system.

---

# Files Submitted

* README.md
* network_security_assessment.md
* nmap_results.txt
* wireshark_capture.pcap

---

# Outcome

Successfully performed a network security assessment using Nmap and Wireshark, identified active services and open ports, analyzed captured network traffic, evaluated potential security risks, and documented the findings with appropriate security recommendations.
