# Project Two: Firewall Policy & Network Segmentation
**CYB-220 | Network Security | Grade: A**

## Objective
Configure host-based and network-based firewall policies in Cisco Packet Tracer, set up a secure FTP server with role-based access controls, and document the security rationale behind each design decision.

---

## Configurations Completed

### 1. Host-Based Firewall Policy
Configured a firewall policy on the host system to restrict communication exclusively to the admin network and the FTP server. All other inbound and outbound connections are blocked by default.

**Rule logic:** Default-deny with explicit allow rules — only approved traffic flows are permitted. This is the most secure baseline posture.

---

### 2. FTP Server Configuration
Set up an FTP server with role-based access permissions:

| User Role | Permissions |
|---|---|
| Regular users | Read, List (view and download only) |
| Administrative users | Read, Write, Delete, Navigate, List (full management) |

**Security value:** Users can only perform actions their role requires. A regular user cannot modify, delete, or overwrite files — limiting accidental or malicious data manipulation.

---

### 3. Network-Based Firewall (Extended ACL)
Configured a network-based firewall using an Extended Access Control List (ACL) to control which devices can communicate with each other across network segments.

**Extended ACLs allow control based on:**
- Source IP address
- Destination IP address
- Protocol (TCP, UDP, ICMP)
- Port number

This granularity means traffic can be permitted or denied at a very specific level — not just "allow all" or "block all."

---

## Security Rationale

### Segmentation
Network segmentation creates clear boundaries between different areas of the network. The combined host-based firewall and network ACL ensure that:
- The admin network can reach the FTP server
- Non-admin segments cannot reach the FTP server
- Lateral movement between segments is controlled and logged

> *"Segmentation limits the blast radius of any single compromise — an attacker who gains access to one segment cannot freely move to others."*

### Least Privilege
Applied at the FTP layer: users receive only the permissions their role requires. Regular users cannot delete or modify files, preventing accidental data loss and limiting the damage of compromised regular-user credentials.

### Isolation
The network-based firewall defines exactly how devices may interact. There are no unintended communication paths — every allowed flow was deliberately configured. This eliminates the "flat network" problem where any device can reach any other device by default.

---

## Skills Demonstrated
`Host-Based Firewall` `Network-Based Firewall` `Extended ACL` `FTP Server Configuration` `Role-Based Access Control` `Network Segmentation` `Least Privilege` `Network Isolation` `Cisco Packet Tracer` `Security Rationale Documentation`
