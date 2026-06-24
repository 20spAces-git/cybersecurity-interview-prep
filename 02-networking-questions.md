# Networking Interview Questions

## What is an IP Address?

Answer:

An IP address is a unique identifier assigned to a device on a network.

Its purpose is to allow devices to communicate with one another.

Example:

192.168.1.1

---

## What is DNS?

Answer:

DNS (Domain Name System) translates domain names into IP addresses.

Example:

google.com → 142.250.x.x

Without DNS, users would need to remember IP addresses instead of website names.

---

## What is DHCP?

Answer:

DHCP (Dynamic Host Configuration Protocol) automatically assigns IP addresses to devices on a network.

Benefits:

- Simplifies network management
- Prevents IP conflicts
- Automates configuration

---

## What is ARP?

Answer:

ARP (Address Resolution Protocol) maps IP addresses to MAC addresses on local networks.

Example:

A device knows an IP address but needs the corresponding MAC address before communication can occur.

---

## What is a MAC Address?

Answer:

A MAC address is a unique hardware identifier assigned to a network interface card (NIC).

Example:

00:1A:2B:3C:4D:5E

---

## What is TCP?

Answer:

TCP (Transmission Control Protocol) is a connection-oriented protocol that provides reliable data transmission.

Features:

- Reliable
- Ordered
- Error Checking

Examples:

- Web Browsing (HTTP/HTTPS)
- Email
- File Transfers

---

## What is UDP?

Answer:

UDP (User Datagram Protocol) is a connectionless protocol that prioritizes speed over reliability.

Features:

- Faster than TCP
- No connection establishment
- No guaranteed delivery

Examples:

- Streaming
- VoIP
- Online Gaming

---

## What is the Difference Between TCP and UDP?

Answer:

TCP:

- Reliable
- Slower
- Connection-Oriented

UDP:

- Faster
- Less Reliable
- Connectionless

---

## What is ICMP?

Answer:

ICMP (Internet Control Message Protocol) is used for network diagnostics and error reporting.

Examples:

- Ping
- Traceroute

---

## What is a Port?

Answer:

A port is a logical communication endpoint used by applications and services.

Examples:

- Port 80 = HTTP
- Port 443 = HTTPS
- Port 53 = DNS
- Port 22 = SSH

---

## What is a Router?

Answer:

A router connects multiple networks and forwards traffic between them.

---

## What is a Switch?

Answer:

A switch connects devices within the same local network and forwards traffic based on MAC addresses.

---

## Common Beginner Interview Question

Question:

What happens when you type google.com into a web browser?

Answer:

1. DNS resolves the domain name to an IP address.
2. The browser establishes a TCP connection.
3. The browser sends an HTTP/HTTPS request.
4. The server responds with the requested webpage.
5. The browser displays the content.

---

## DFIR Relevance

Networking knowledge helps investigators:

- Analyze traffic
- Identify suspicious connections
- Investigate attacks
- Track malicious activity
- Understand attacker behavior

---
---

## What is the Difference Between TCP and UDP?

Answer:

*   **TCP (Transmission Control Protocol):** Connection-oriented. It guarantees delivery of data through a three-way handshake, error-checking, and retransmission of lost packets. Used where accuracy matters (e.g., HTTPS, SSH, SFTP).
*   **UDP (User Datagram Protocol):** Connectionless. It sends packets ("datagrams") without establishing a connection or verifying delivery. It is much faster but unreliable. Used where speed matters (e.g., video streaming, gaming, DNS).

---

## What is the OSI Model and Can You Name the Layers?

Answer:

The OSI (Open Systems Interconnect) model is a conceptual framework used to understand network interactions across 7 layers. 

1. **Physical:** Transmits raw bit streams over physical medium (Cables, Hubs).
2. **Data Link:** Defines format of data on the network; handles MAC addresses (Switches).
3. **Network:** Handles path determination and logical routing (IP addresses, Routers).
4. **Transport:** Manages end-to-end connections and reliability (TCP, UDP).
5. **Session:** Manages and terminates connections between applications.
6. **Presentation:** Ensures data is in a usable format; handles encryption and compression (SSL/TLS).
7. **Application:** Human-computer interaction layer where applications access network services (HTTP, DNS, FTP).

---

## What is ARP and How Does It Work?

Answer:

**ARP (Address Resolution Protocol)** resolves a known IPv4 address to a physical MAC address on a local network. When a device wants to communicate with another device on the same subnet, it broadcasts an ARP request asking, "Who has this IP?" The device with that IP replies with its MAC address, which is then cached locally.

---

## What is the Difference Between a Hub, a Switch, and a Router?

Answer:

*   **Hub:** Connects devices on a network but is "dumb." It broadcasts all incoming data packets to every single port, creating unnecessary traffic and security risks.
*   **Switch:** Connects devices on the *same* local network (LAN). It learns MAC addresses and intelligently forwards data only to the specific device it's intended for (Layer 2).
*   **Router:** Connects completely *different* networks together (e.g., connecting your home LAN to the internet). It routes data based on IP addresses (Layer 3).
Status: Complete ✅
