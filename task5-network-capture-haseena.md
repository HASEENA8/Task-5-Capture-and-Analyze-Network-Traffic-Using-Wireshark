# 🛠️ Task 5 – Network Traffic Capture and Analysis using Wireshark

## 🎯 Objective
To capture live network traffic using Wireshark and analyze at least three network protocols: DNS, TCP, and HTTP.

---

## 🧰 Tools Used
- OS: Parrot Security OS (in VirtualBox)
- Tool: Wireshark 3.4.10
- Website visited: [http://neverssl.com](http://neverssl.com)
- Commands: `ping google.com`

---

## 🌐 Protocols Identified and Analyzed

### 1. 🟡 DNS (Domain Name System)
- **Purpose**: Resolves domain names (like google.com) into IP addresses.
- **Captured Packets**: Frame 45–69
- **Example Packet**:
  - **Frame**: `69`
  - **Source**: `192.XXX.X.X`
  - **Destination**: `192.XXX.X.X`
  - **Info**: Standard DNS response to query

---

### 2. 🔵 TCP (Transmission Control Protocol)
- **Purpose**: Establishes reliable communication between systems.
- **Captured Packets**: Frames 46–77
- **Example Packet**:
  - **Frame**: `73`
  - **Source**: `192.XXX.X.X`
  - **Destination**: `104.107.221.82`
  - **Info**: TCP segment used in HTTP transfer (port 80)

---

### 3. 🔴 HTTP (HyperText Transfer Protocol)
- **Purpose**: Used for web traffic over port 80.
- **Captured Packets**: Frames 73, 74, 75, 76, 939
- **Example Packet**:
  - **Frame**: `73`
  - **Source**: `192.XXX.X.X`
  - **Destination**: `104.107.221.82`
  - **Info**: HTTP GET / request (non-encrypted)

---

## 📄 Output Files

| File Name             | Description                  |
|-----------------------|------------------------------|
| `Haseena.pcap`        | Wireshark packet capture file |
| `README.md`           | This analysis report          |

---

## 📸 Screenshots Included
- HTTP traffic (`http` filter applied)
- TCP traffic (`tcp` filter applied)
- DNS traffic (`dns` filter applied)

---

## 📌 Observations
- The HTTP packets were successfully captured due to the use of a non-HTTPS website.
- DNS requests resolved IPs like `google.com` and `neverssl.com`.
- TCP segments showed the connection setup and HTTP data transfer between client and server.

---

## ✅ Conclusion
The task helped in identifying how different network protocols interact:
- DNS resolves domains,
- TCP handles reliable connections,
- HTTP carries application-layer data.

This demonstrates real-world packet behavior and filtering in a live network environment using Wireshark.

