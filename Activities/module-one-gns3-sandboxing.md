# Module One: GNS3 Sandboxing — Network Topology Setup
**CYB-220 | Network Security**

## Objective
Build and configure a virtual network in GNS3 consisting of two Windows PCs, a Windows Server, and a Cisco 3745 router — then verify full connectivity across all devices using ping tests.

---

## Topology
- **PC1_TestNetwork** — Windows PC, connected to router
- **PC2_TestNetwork** — Windows PC, connected to router
- **Server_TestNetwork** — Windows Server, connected to router
- **Router_TestNetwork** — Cisco 3745, connecting all devices

IP addresses assigned per provided table on all interfaces.

---

## Ping Test Results

| Test | Result |
|---|---|
| PC1 → PC1 Gateway | ✅ Success |
| PC1 → PC2 Gateway | ✅ Success |
| PC1 → PC2 | ✅ Success |
| PC2 → PC1 | ✅ Success |
| PC2 → Server | ✅ Success |
| Server → PC1 | ✅ Success |
| Server → PC2 | ✅ Success |
| PC1 → Server | ✅ Success |

Full mesh connectivity confirmed across all devices and gateways.

---

## Why GNS3 for Security Work?
GNS3 allows security professionals to build and test network configurations in a safe, isolated sandbox — without risk to production systems. This is the same approach used in professional security labs, penetration testing environments, and training programs.

## Skills Demonstrated
`GNS3` `Virtual Network Configuration` `Cisco 3745 Router` `IP Assignment` `Ping Testing` `Network Topology Design` `Sandboxing`
