# Network Traffic Analysis and Suspicious Activity Detection With Wireshark

## Introduction

The current project is dedicated to the analysis of normal network traffic with Wireshark and the detection of patterns related to suspicious activities.

## Objectives

- Capture and analyze normal network traffic.
- Analyze DNS requests and answers.
- Look at the TCP three-way handshake process.
- Check the TLS Client Hello packet and the SNI data.
- Analyze protocol distribution.
- Perform a controlled SYN port scan with Nmap.
- Detect patterns of SYN scan and RST/ACK responses.

## Tools Used

- Wireshark 4.6.8
- Nmap 7.991
- Npcap 1.88
- Windows 11

## Methodology

1. Captured normal browsing traffic on the Wi-Fi interface.
2. Analyzed DNS requests and answers.
3. Looked at the TCP three-way handshake.
4. Checked the TLS 1.3 Client Hello and SNI data.
5. Conducted the controlled SYN scan towards `127.0.0.1` ports 20-100.
6. Captured and analyzed SYN probes and RST/ACK responses with Wireshark.
7. Viewed the protocol hierarchy of the baseline capture.

## Key Observations

- Normal traffic had DNS, TCP, UDP, QUIC, TLS, IPv4, and IPv6 traffic.
- DNS requests and responses were seen in normal traffic.
- The TLS Client Hello message provided the metadata of the website in the form of SNI such as `www.youtube.com`.
- There were SYN probes to different ports, which were indicative of a SYN scan.
- RST/ACK packets were indicative of closed ports in the scan test.
## Project Structure

```text
Network-Traffic-Analysis/
├── captures/
│   ├── normal_traffic_baseline.pcapng
│   └── port_scan_lab.pcapng
├── screenshots/
│   ├── 01_dns_query.png
│   ├── 02_dns_response.png
│   ├── 03_tcp_handshake.png
│   ├── 04_tls_client_hello.png
│   ├── 05_syn_scan_detection.png
│   ├── 06_scan_rst_responses.png
│   └── 07_protocol_hierarchy.png
├── report/
│   └── Network_Traffic_Analysis_Report.pdf
└── README.md
