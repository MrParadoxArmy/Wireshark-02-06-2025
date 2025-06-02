# 📡 Wireshark Network Traffic Capture & Protocol Analysis

## 🧭 Objective

This project demonstrates live network traffic capture and protocol analysis using Wireshark. The primary focus is on identifying and interpreting traffic from key protocols including DNS, TCP, ICMP, and TLS. The exercise aims to provide hands-on experience with real-time packet inspection and network behavior analysis across OSI model layers.

---

## 🧰 Tools & Environment

- **Network Analyzer:** Wireshark
- **Operating System:** Windows 10/11
- **Interface Type:** Ethernet/Wi-Fi
- **Supplementary Tools:** Windows Command Prompt (`ping`, `nslookup`)

---

## 🛠️ Procedure

1. **Wireshark Setup**
   - Installed and configured Wireshark.
   - Launched with administrative privileges to allow full interface access.

2. **Traffic Generation**
   - Visited multiple websites to generate HTTPS (TLS) and DNS traffic.
   - Executed `ping google.com` to generate ICMP packets.
   - Observed automatic TCP connections during webpage loading.

3. **Packet Capture**
   - Selected the active network interface and started live capture.
   - Ran traffic for approximately one minute.
   - Stopped and saved the capture session as `packet_capture.pcapng`.

4. **Filtering & Analysis**
   - Applied Wireshark display filters:
     - `dns` – to isolate domain name resolution queries
     - `tcp` – to view TCP handshake and session data
     - `icmp` – to inspect echo requests/replies
     - `tls` – to observe encrypted HTTPS connections
   - Analyzed packet headers, flags, and protocol payloads.

---

## 📁 Deliverables

- `packet_capture.pcapng` – Raw packet capture file
- `report.md` – Detailed breakdown of protocol interactions and sample packet insights
- `README.md` – Workflow documentation and analysis summary

---

## 🧩 Protocols Observed

| Protocol | OSI Layer | Purpose | Notes |
|----------|-----------|---------|-------|
| **DNS**  | Layer 7 – Application | Resolves domain names to IPs | Primarily UDP, some TCP fallback |
| **TCP**  | Layer 4 – Transport   | Reliable connection-based transport | Captured full 3-way handshake and ACKs |
| **ICMP** | Layer 3 – Network     | Network diagnostics (ping) | Echo requests and replies observed |
| **TLS**  | Layer 6 – Presentation| Secure encrypted communication | TLS 1.2 handshake and certificate exchange seen |

---

## 📊 Highlights & Insights

- **DNS:** Observed A and AAAA queries with corresponding responses from public DNS (e.g., `8.8.8.8`).
- **TCP:** Captured connection initiation (SYN), establishment (SYN-ACK), and teardown (FIN/ACK).
- **ICMP:** Confirmed live network reachability through echo request/reply cycle.
- **TLS:** Identified encrypted sessions with visible certificate metadata and key exchange.

---

## 🏁 Conclusion

Through this lab, key practical skills were gained:
- Navigating and configuring Wireshark for real-time capture.
- Using filters to focus on specific protocols.
- Understanding packet structure across OSI layers.
- Recognizing encrypted vs plaintext traffic patterns.

This foundational analysis supports more advanced activities such as traffic anomaly detection, intrusion analysis, and cybersecurity auditing.

---

## 📎 Additional Notes

- Ensure you run Wireshark as administrator for full interface access.
- TLS decryption requires session keys (not covered in this lab).
- Packet timestamps and sizes are useful for performance diagnostics and latency tracking.

