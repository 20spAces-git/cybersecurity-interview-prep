# Wireshark Interview Questions

## What is Wireshark?

Answer:

Wireshark is a network protocol analyzer used to capture and inspect network traffic in real time.

Security professionals use Wireshark to:

- Troubleshoot networks
- Analyze traffic
- Investigate incidents
- Detect suspicious activity

---

## What is a Packet?

Answer:

A packet is a unit of data transmitted across a network.

Packets contain:

- Source Address
- Destination Address
- Protocol Information
- Data Payload

---

## What is Packet Capture?

Answer:

Packet capture is the process of collecting network traffic for analysis.

Wireshark captures packets and allows analysts to inspect communication between devices.

---

## What Protocols Have You Analyzed in Wireshark?

Answer:

I have analyzed:

- DNS
- ARP
- ICMP
- TCP

through hands-on Wireshark labs and packet analysis exercises.

---

## What is a Display Filter?

Answer:

A display filter allows analysts to view specific traffic within a packet capture.

Examples:

dns

tcp

icmp

arp

---

## How Would You Filter DNS Traffic?

Answer:

Display Filter:

dns

Purpose:

Displays only DNS-related traffic.

---

## How Would You Filter TCP Traffic?

Answer:

Display Filter:

tcp

Purpose:

Displays only TCP packets.

---

## How Would You Filter ICMP Traffic?

Answer:

Display Filter:

icmp

Purpose:

Displays ping and other ICMP-related traffic.

---

## What Information Can You Learn From a Packet?

Answer:

A packet can reveal:

- Source IP Address
- Destination IP Address
- Source Port
- Destination Port
- Protocol
- Packet Size
- Communication Details

---

## Why is DNS Important During an Investigation?

Answer:

DNS traffic can reveal:

- Websites visited
- Suspicious domains
- Malware communications
- Command-and-control activity

---

## Why is ARP Important During an Investigation?

Answer:

ARP can help identify:

- Devices on a network
- MAC addresses
- Potential ARP spoofing attacks

---

## Why is TCP Important During an Investigation?

Answer:

TCP allows investigators to:

- Track connections
- Analyze sessions
- Review communications
- Identify suspicious activity

---

## What Would You Look For in Suspicious Network Traffic?

Answer:

I would look for:

- Unknown IP addresses
- Unusual DNS requests
- Unexpected outbound connections
- Large file transfers
- Repeated failed connections
- Connections to suspicious domains

---

## Beginner Interview Question

Question:

Have you used Wireshark before?

Answer:

Yes.

I have completed hands-on Wireshark labs involving:

- Packet Capture
- DNS Analysis
- ARP Analysis
- ICMP Analysis
- TCP Analysis

I used filters to inspect network traffic and understand how devices communicate across a network.

---

## DFIR Relevance

Wireshark is commonly used during:

- Incident Response
- Threat Hunting
- Network Forensics
- Malware Investigations
- Security Monitoring

---
---

## What is the Difference Between a Display Filter and a Capture Filter?

Answer:

*   **Capture Filter:** Applied *before* the packet capture begins. It dictates exactly what traffic Wireshark saves to the buffer (e.g., `host 192.168.1.1` or `port 80`). It reduces file size and CPU usage but means uncaptured traffic is lost forever. Uses BPF (Berkeley Packet Filter) syntax.
*   **Display Filter:** Applied *after* traffic has already been captured. It merely hides packets from view based on specified criteria (e.g., `http.request.method == "POST"` or `ip.addr == 10.0.0.5`) without deleting any data.

---

## How Would You Use Wireshark to Follow a Cleartext Stream (like HTTP or Credentials)?

Answer:

I would locate a packet belonging to the communication of interest, right-click it, select **Follow**, and then choose **TCP Stream** (or HTTP/TLS Stream depending on the protocol). This opens a window that reconstructs the entire conversation in chronological order, displaying the ASCII text data exchanged between the client (usually in red) and the server (usually in blue), making it easy to spot plaintext passwords, commands, or data transfers.

---

## What Wireshark Indicator or Window Helps You Identify High-Level Network Issues Quickly?

Answer:

I look at the **Expert Info** window (`Analyze -> Expert Information`). Wireshark automatically categorizes specific network behaviors into four severity levels:
*   **Chat:** Normal workflow (e.g., a standard TCP window update).
*   **Note:** Notable events (e.g., an HTTP text/html return code).
*   **Warn:** Unusual behaviors (e.g., application errors or unexpected TCP window sizes).
*   **Error:** Serious issues (e.g., malformed packets or severe connection drops).

---

## What Filter Would You Use to Find a Potential TCP SYN Flood Attack?

Answer:

I would filter for TCP SYN packets that do not have the ACK flag set using `tcp.flags.syn == 1 and tcp.flags.ack == 0`. In a normal connection handshake, these should be followed quickly by a SYN-ACK. If the capture shows a massive volume of these packets from a single or random IP address without corresponding ACKs, it indicates a SYN flood (DoS) attempt.

Status: Complete ✅
