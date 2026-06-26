# Task 1: Basic Network Scanning with Nmap

## Objective

The objective of this task was to perform a basic network scan using Nmap to identify open ports and running services on a local Windows 11 machine. This task also involved analyzing the discovered services, understanding their purpose, and documenting the findings professionally.

---

## Tools Used

- Nmap 7.99
- Windows 11
- Command Prompt (CMD)

---

## Task Execution

### Step 1: Install Nmap

Nmap was downloaded from the official Nmap website and installed successfully on the Windows 11 system using the default installation settings.

> **Observation:** Nmap is an open-source network scanning tool widely used for network discovery and security auditing.

---

### Step 2: Verify Nmap Installation

After installation, the following command was executed to verify that Nmap was installed successfully.

```bash
nmap --version
```

**Output**

```text
Nmap version 7.99
```

> **Observation:** The displayed version confirms that Nmap was installed successfully and is ready for use.

---

### Step 3: Identify the Target IP Address

Before performing the network scan, the IPv4 address of the local machine was identified using the following command.

```bash
ipconfig
```

**Target IPv4 Address**

```text
192.168.0.101
```

> **Observation:** This IPv4 address was used as the target for the Nmap scan.

---

### Step 4: Perform a Basic Network Scan

A basic TCP port scan was performed using the following command.

```bash
nmap 192.168.0.101
```

**Purpose:** This command scans the target system to identify open TCP ports and the services associated with them.

---

### Step 5: Perform Service Version Detection

To identify the software versions running on the open ports, the following command was executed.

```bash
nmap -sV 192.168.0.101
```

**Purpose:** The `-sV` option enables service version detection, allowing Nmap to determine the application or software running behind each open port.

---

### Step 6: Save the Scan Results

The scan results were saved into a text file using the following command.

```bash
nmap -sV 192.168.0.101 -oN nmap_scan_results.txt
```

**Generated File**

```text
nmap_scan_results.txt
```

> **Observation:** Saving the scan results makes future analysis and documentation easier.

---

## Screenshots

### Nmap Installation Verification

![Nmap Version](screenshots/nmap_version.png)

### IPv4 Address Identification

![IP Configuration](screenshots/ipconfig.png)

### Basic Network Scan

![Basic Network Scan](screenshots/basic_network_scan.png)

### Service Version Detection

![Service Version Scan](screenshots/service_version_scan.png)

---

## Scan Results

| Port | State | Service | Version |
|------|:-----:|---------|---------|
| 135 | Open | MSRPC | Microsoft Windows RPC |
| 139 | Open | NetBIOS-SSN | Microsoft Windows NetBIOS Session Service |
| 445 | Open | Microsoft-DS | Windows File Sharing Service |
| 2869 | Open | HTTP | Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP) |
| 3306 | Open | MySQL | MySQL (Unauthorized) |

> **Observation:** The scan identified five open TCP ports running various Windows and database services.

---

## Findings

### Port 135 – MSRPC

- Used for Microsoft Remote Procedure Call (RPC).
- Supports communication between Windows services.
- Should be monitored for unauthorized remote access.

### Port 139 – NetBIOS

- Used for Windows file and printer sharing.
- May expose shared resources if not properly secured.

### Port 445 – SMB

- Used by the Server Message Block (SMB) protocol.
- Supports Windows file sharing and network communication.
- Keeping SMB updated is important because it has historically been targeted by malware.

### Port 2869 – HTTP

- Used by Microsoft's HTTPAPI service.
- Commonly associated with SSDP and UPnP device discovery.

### Port 3306 – MySQL

- Default port used by the MySQL Database Server.
- Indicates that a MySQL service is running.
- Should be protected with strong credentials and restricted network access.

---

## Security Recommendations

- Disable unused network services whenever possible.
- Restrict SMB and NetBIOS access to trusted systems only.
- Use strong authentication for MySQL and other database services.
- Regularly update Windows and network services.
- Configure firewall rules to block unnecessary ports.
- Perform periodic network scans to identify newly exposed services.

---

## Learning Outcome

Through this task, I learned how to:

- Install and verify Nmap on Windows.
- Identify the IPv4 address of a target system.
- Perform basic network scanning.
- Detect service versions using Nmap.
- Analyze open ports and the services running on them.
- Understand the security implications of exposed services.
- Document scan results in a professional GitHub repository.

---

## Repository Structure

```text
OIBSIP/
│
└── BajiShaik_Task1/
    │
    ├── README.md
    ├── nmap_scan_results.txt
    │
    └── screenshots/
        ├── nmap_version.png
        ├── ipconfig.png
        ├── basic_network_scan.png
        └── service_version_scan.png
```

---

## Conclusion

This task successfully demonstrated how to use Nmap to perform basic network reconnaissance on a Windows 11 system. The scan identified active services, open ports, and their associated software versions, providing valuable insight into the system's network exposure. Regular network scanning is an essential cybersecurity practice for identifying potential security risks and maintaining a secure environment.

---

## Author

**Baji Shaik**

Security Analyst Intern

Oasis Infobyte
