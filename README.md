# 🔐 CYB-220: Network Security
**Southern New Hampshire University | Grade: A | Term: 2025 C-1 (Jan – Mar)**

> Hands-on network security course covering common network-based attacks and defenses, intrusion detection/prevention systems, firewall policy configuration, Group Policy hardening, virtual system sandboxing with GNS3, and information flow controls.

---

## 📋 Course Overview
This course moved from networking concepts into active network defense. Using GNS3 and Cisco Packet Tracer, I configured real security controls — host-based and network-based firewalls, FTP server access policies, Group Policy hardening, and intrusion detection systems. Every project was scenario-based, requiring both technical implementation and written justification of security design decisions.

---

## 📁 Repository Structure

```
network-security-cyb220/
│
├── projects/
│   ├── project-one-virtual-system-hardening.md
│   ├── project-two-firewall-policy-and-segmentation.md
│   └── project-three-nids-recommendation.md
│
├── activities/
│   ├── module-one-gns3-sandboxing.md
│   ├── module-three-group-policy-hardening.md
│   ├── module-four-ftp-server-access-control.md
│   └── module-five-technology-evaluation-criteria.md
│
└── README.md
```

---

## 📝 Projects

### 🔵 Project One — Virtual System Hardening
Hardened a Windows virtual machine in GNS3 by configuring system-level security settings across UAC, password policy, audit policy, user rights, logon banners, and firewall profiles.

**Controls configured:**
- Windows UAC prompt settings
- Local password policy (complexity, length, expiration)
- Desktop background user rights (disabled non-admin changes)
- Local audit policy (tracking logon events, privilege use)
- Default logon banner with required affirmation
- Windows Firewall profile configuration
- Router and kiosk PC network configurations

**Skills demonstrated:** Windows hardening, Group Policy, UAC, audit logging, firewall configuration, virtual machine administration

---

### 🔵 Project Two — Firewall Policy & Network Segmentation
Configured host-based and network-based firewall policies in Cisco Packet Tracer, set up an FTP server with role-based access controls, and documented the security rationale for each design decision.

**Key configurations:**
- **Host-based firewall:** Restricted communication to admin network and FTP server only
- **FTP server access:** Regular users → read/list only; admins → full file management
- **Network-based firewall:** Extended ACL controlling inter-segment traffic flow

**Security principles applied:**
- **Segmentation:** Firewall policies and ACLs create clear network boundaries, limiting lateral movement
- **Least Privilege:** FTP users receive only the permissions their role requires
- **Isolation:** Network-based firewall defines exactly how devices interact — no unauthorized paths

**Skills demonstrated:** Host-based firewall policy, network ACLs, FTP server configuration, role-based access, network segmentation, security rationale documentation

---

### 🔵 Project Three — NIDS Recommendation
Evaluated network protection technologies for a financial institution (150–200 employees, 4 network segments, moderate-to-high risk tolerance) and recommended a Network-Based Intrusion Detection System (NIDS).

**Recommendation: NIDS (Snort/Suricata)**

| Factor | Assessment |
|---|---|
| **Effectiveness** | Real-time monitoring across all 4 segments (sales, acquisitions, HR, IT); detects unauthorized access and abnormal traffic patterns |
| **Cost** | Open-source tools (Snort, Suricata) — powerful capability with minimal financial investment |
| **Staffing** | Alert-based monitoring suits a small IT team; doesn't require extensive configuration overhead |
| **Principle applied** | Least Privilege — NIDS provides visibility without actively interfering with traffic; supports correct segment segregation |

**Resource requirements identified:** Dedicated server with adequate processing/storage; training for 2 team members on NIDS configuration and alert management.

**Skills demonstrated:** Technology evaluation, NIDS vs IPS analysis, open-source security tools (Snort, Suricata), organizational risk assessment, written security recommendation

---

## 🗂️ Activities

### Module One — GNS3 Sandboxing (Network Topology Setup)
Built a virtual network topology in GNS3 with two Windows PCs, a Windows Server, and a Cisco 3745 router. Assigned IP addresses across all interfaces and verified full connectivity with ping tests between all devices.

**Ping tests completed:**
- PC1 ↔ PC2 ✅
- PC1 ↔ Server ✅
- PC2 ↔ Server ✅
- All gateway reachability tests ✅

---

### Module Three — Group Policy Hardening
Used Windows Group Policy (GPO) to harden a virtual PC by identifying and configuring the correct GPO paths for each security setting.

| Policy | GPO Path |
|---|---|
| Hide user accounts in Control Panel | User Configuration\Administrative Templates\Control Panel |
| Remove Task Manager | User Configuration\Administrative Templates\System\Ctrl+Alt+Del Options |
| Remove Recycle Bin from desktop | User Configuration\Administrative Templates\Desktop |
| Disable delete notifications on all volumes | Computer Configuration\Administrative Templates\System\Filesystem |

**Skills demonstrated:** Group Policy administration, Windows hardening, GPO path navigation, system security configuration

---

### Module Four — FTP Server Access Control Lab
Configured and tested FTP server access in Cisco Packet Tracer using CLI commands. Verified access permissions, connected to the FTP server from an admin workstation, and enumerated directory contents.

**Key findings:**
- Default FTP user (cisco) permissions: **RWDNL** (Read, Write, Delete, Navigate, List)
- Successfully connected: `FTP 10.1.10.5` from Server1_Admin
- Directory listing retrieved and documented
- Identified security risk: default credentials should always be changed before deployment

**Skills demonstrated:** FTP configuration, CLI access, permission analysis, default credential risk identification

---

### Module Five — Technology Evaluation Criteria Worksheet
Evaluated network security technologies against structured criteria for a financial institution scenario. Assessment covered:
- Ability to identify network-connected systems
- OS detection capability for vulnerability/patch management
- Application-layer monitoring for data exfiltration detection
- Encrypted malicious traffic detection
- Organizational fit (budget, staffing, risk tolerance)

**Skills demonstrated:** Security technology evaluation, organizational risk analysis, structured decision-making framework

---

## 💡 Key Concepts Mastered
- Host-based and network-based firewall configuration
- Extended ACLs for traffic control
- FTP server security and access control
- Windows Group Policy (GPO) hardening
- GNS3 virtual network sandboxing
- NIDS vs IPS — detection vs. prevention tradeoffs
- Open-source IDS tools: Snort, Suricata
- Network segmentation and isolation principles
- Security technology evaluation frameworks
- Least Privilege applied at network and application layers

---

## 🛠️ Tools Used
- **GNS3** — virtual network sandbox
- **Cisco Packet Tracer** — network simulation
- **Windows Group Policy (GPO)** — system hardening
- **Cisco 3745 Router CLI** — interface and routing configuration
- **Snort / Suricata** — referenced open-source NIDS tools

## 📚 Course
- **CYB-220** — Network Security | Grade: A | SNHU 2025
