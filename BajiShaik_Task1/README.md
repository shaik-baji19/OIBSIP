# Basic Network Scanning with Nmap

## Objective

The objective of this task is to perform a network scan using Nmap and identify open ports and services running on the target machine.

> **Note:** Network scanning is one of the first steps in cybersecurity assessments and helps identify exposed services on a system.

---

## Tool Used

* **Nmap 7.99**

> **Note:** Nmap is a widely used open-source tool for network discovery and security auditing.

---

## Prerequisites

* Nmap installed on the system.
* Access to the target machine within the local network.
* Basic knowledge of networking concepts.

---

## Target

**IP Address:** `192.168.0.101`

> **Observation:** The target system is a Windows 11 machine within a local network environment.

---

## Commands Executed

### 1. Basic Port Scan

```bash
nmap 192.168.0.101
```

**Purpose:** Used to identify open ports and associated services running on the target machine.

### 2. Service Version Detection

```bash
nmap -sV 192.168.0.101
```

**Purpose:** The `-sV` option provides additional information about the versions of services running on open ports.

> **Observation:** Service version detection helps administrators understand what software is exposed to the network.

---

## Screenshots

### Basic Port Scan

![Basic Network Scan](screenshots/basic_network_scan.png)

### Service Version Detection

![Service Version Scan](screenshots/service_version_scan.png)

---

## Scan Results

| Port | State | Service      | Version                                   |
| ---- | :---: | ------------ | ----------------------------------------- |
| 135  |  Open | msrpc        | Microsoft Windows RPC                     |
| 139  |  Open | netbios-ssn  | Microsoft Windows NetBIOS Session Service |
| 445  |  Open | microsoft-ds | Windows File Sharing Service              |
| 2869 |  Open | HTTP         | Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)   |
| 3306 |  Open | MySQL        | MySQL (unauthorized)                      |

> **Observation:** A total of five open TCP ports were identified during the scan.

---

## Findings

### Port 135 (MSRPC)

Used by Microsoft Windows for Remote Procedure Calls and communication between services.

**Security Note:** This service is required by many Windows components and should be monitored for unusual activity.

### Port 139 (NetBIOS)

Used for file and printer sharing across Windows networks.

**Security Note:** If file sharing is not required, disabling NetBIOS can help reduce the attack surface.

### Port 445 (SMB)

Used by Microsoft SMB protocol for file sharing and network communication.

**Security Note:** SMB services should be kept updated because they have historically been targeted by malware and ransomware attacks.

### Port 2869 (HTTP)

Associated with SSDP/UPnP services used for device discovery.

**Observation:** This service supports automatic discovery of devices on the local network.

### Port 3306 (MySQL)

Default port for MySQL database services.

**Observation:** The scan indicates that a MySQL service is currently running on the target machine.

**Security Note:** Database services should be protected using strong credentials and restricted access policies.

---

## Security Recommendations

* Disable unused network services whenever possible.
* Restrict SMB and NetBIOS access to trusted devices only.
* Use strong authentication for database services.
* Regularly update operating systems and network services.
* Perform periodic network scans to identify newly exposed services.
* Configure firewalls to limit unnecessary access to open ports.

---

## Learning Outcome

Through this task, I learned how to:

* Install and use Nmap on Windows.
* Perform basic network scanning.
* Identify open ports and active services.
* Perform service version detection.
* Analyze scan results and understand their security implications.
* Document findings in a professional manner.

---

## Repository Structure

```text
BajiShaik_Task1/
│
├── README.md
├── nmap_scan_results.txt
└── screenshots/
    ├── basic_network_scan.png
    └── service_version_scan.png
```

---

## Conclusion

The Nmap scan successfully identified five open ports and their associated services on the target Windows 11 system. The results provide valuable insight into exposed network services and help assess potential security risks.

> **Final Observation:** Regular network scanning is an important cybersecurity practice that helps identify unnecessary services, improve system security, and maintain network visibility.

---

## Author

**Baji Shaik**

Cybersecurity Internship Program

Oasis Infobyte
