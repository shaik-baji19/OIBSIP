# Task 8: Network Traffic Capture and Packet Analysis using Wireshark

## 📌 Objective

The objective of this task was to capture live network traffic using **Wireshark**, analyze the captured packets, and understand how network communication takes place between devices. This task also involved filtering specific protocols, inspecting packet details, and documenting the findings from a cybersecurity perspective.

---

## 🛠️ Tools Used

- Wireshark 4.6.6
- Windows 11
- Google Chrome
- Wi-Fi Network Adapter

---

## 🚀 Task Execution

### Step 1: Install Wireshark

Wireshark was downloaded from the official website and installed successfully on the Windows 11 system using the default installation settings.

**Observation**

Wireshark is one of the most widely used network protocol analyzers that allows users to capture, inspect, and troubleshoot network traffic in real time.

---

### Step 2: Launch Wireshark

After installation, Wireshark was launched successfully.

The available network interfaces were displayed, and the active **Wi-Fi** interface was selected for packet capture.

**Observation**

Selecting the active network interface ensures that only the packets transmitted through that interface are captured.

---

### Step 3: Start Packet Capture

Packet capturing was started by double-clicking the active **Wi-Fi** interface.

To generate network traffic, several websites were opened using Google Chrome while Wireshark continuously captured the packets.

**Observation**

During packet capture, different network protocols such as **TCP**, **UDP**, **TLSv1.2**, **QUIC**, and **mDNS** were observed.

---

### Step 4: Stop Packet Capture

After sufficient traffic had been captured, the packet capture process was stopped using the **Stop Capture** button.

The captured packets were then available for further analysis.

---

### Step 5: Apply TCP Display Filter

To analyze only TCP packets, the following display filter was applied:

```text
tcp
```

**Purpose**

The TCP display filter hides unrelated packets and displays only those using the **Transmission Control Protocol (TCP)**.

---

### Step 6: Inspect Packet Details

A TCP packet was selected from the packet list for detailed inspection.

The following protocol layers were examined:

- Frame
- Ethernet II
- Internet Protocol Version 6 (IPv6)
- Transmission Control Protocol (TCP)

**Observation**

Each packet contains protocol information arranged in layers according to the TCP/IP networking model.

---

### Step 7: Document the Results

The captured network traffic was analyzed using Wireshark, and screenshots were taken to document the packet capture process, TCP filtering, and packet inspection for the final report.

---

## 📸 Screenshots

The screenshots demonstrating the task execution are available in the **screenshots/** directory.

The folder contains:

- `wireshark_home.png` – Wireshark launched successfully.
- `network_capture.png` – Live network traffic capture.
- `tcp_packets.png` – TCP display filter applied.
- `packet_details.png` – Detailed inspection of a selected TCP packet.

---

## 📊 Packet Analysis

The captured network traffic contained multiple network protocols that were identified and analyzed using Wireshark.

| Protocol | Description |
|----------|-------------|
| TCP | Reliable connection-oriented communication protocol |
| UDP | Lightweight connectionless communication protocol |
| TLSv1.2 | Encrypts network communication (HTTPS) |
| QUIC | Modern transport protocol used by HTTP/3 |
| mDNS | Multicast DNS used for local device discovery |
| IPv6 | Internet Protocol Version 6 addressing |

---

## 🔍 Findings

### TCP

The majority of captured packets used the **Transmission Control Protocol (TCP)**, which provides reliable and ordered communication between network devices.

---

### TLSv1.2

Several packets contained **TLSv1.2 Application Data**, indicating that modern web traffic is encrypted before transmission.

This prevents attackers from reading sensitive information exchanged between systems.

---

### UDP

UDP packets were also observed.

Unlike TCP, UDP provides faster communication without guaranteeing packet delivery.

---

### mDNS

Multicast DNS packets were detected during the capture.

These packets are commonly used by devices for service discovery within a local network.

---

### IPv6

The captured packets primarily used **Internet Protocol Version 6 (IPv6)**.

Modern operating systems prefer IPv6 whenever it is available on the network.

---

## 🛡️ Security Observations

- Most modern web traffic is encrypted using TLS.
- Packet capture allows administrators to monitor network activity.
- TCP filtering simplifies traffic analysis.
- Network monitoring helps detect abnormal communication.
- Packet analysis assists in troubleshooting network issues and identifying suspicious traffic.

---

## 📚 Learning Outcomes

Through this task, I learned how to:

- Install and configure Wireshark.
- Capture live network traffic.
- Select the correct network interface.
- Filter captured packets using display filters.
- Analyze TCP packets.
- Understand different network protocols.
- Inspect captured packets using Wireshark.
- Document network analysis professionally.

---

## 📂 Repository Structure

```text
OIBSIP/
│
└── BajiShaik_Task8/
    │
    ├── README.md
    │
    └── screenshots/
        ├── wireshark_home.png
        ├── network_capture.png
        ├── tcp_packets.png
        └── packet_details.png
```
---

## ✅ Conclusion

This task successfully demonstrated the process of capturing and analyzing live network traffic using **Wireshark**. Different protocols such as **TCP, UDP, TLSv1.2, QUIC, mDNS, and IPv6** were identified during packet capture. Applying protocol filters and inspecting packet details provided valuable insight into how data travels across a network.

Network packet analysis is an essential cybersecurity practice that enables security professionals to monitor network activity, troubleshoot communication issues, identify suspicious behavior, and strengthen overall network security.

---

## 👨‍💻 Author

**Baji Shaik**

Security Analyst Intern

**Oasis Infobyte**
