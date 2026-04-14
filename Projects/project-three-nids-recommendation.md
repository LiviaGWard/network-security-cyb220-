# Project Three: NIDS Recommendation
**CYB-220 | Network Security | Grade: A**

## Scenario
A financial institution with 150–200 employees and 75+ clients. The network is structured across four segments: Sales, Acquisitions, HR, and IT — with restricted access between them. The IT team has 5 members (including 2 recent graduates). Unauthorized access attempts have already occurred. Budget is constrained and operational disruption must be minimized.

**Risk tolerance:** Moderate to high — financial institutions are prime targets for cyberattacks and the organization has already seen unauthorized access activity.

---

## Security Design Principle Applied: Least Privilege
The Principle of Least Privilege guided the technology recommendation. Users and systems should only have access to what they need — and monitoring should be targeted and proportional. A NIDS provides visibility across network segments without actively interfering with traffic, supporting correct segment segregation while staying within the team's capabilities.

---

## Recommendation: Network-Based Intrusion Detection System (NIDS)

### Why NIDS Over Other Options?

| Technology | Pros | Cons |
|---|---|---|
| **NIDS** ✅ | Real-time monitoring, cost-effective (open-source), low operational overhead, segment-wide visibility | Cannot block threats automatically |
| IPS | Blocks threats in real time | Higher cost, more complex, risk of false positives blocking legitimate traffic |
| Host-based IDS | Per-device visibility | Doesn't scale well across 150-200 endpoints with a small team |

### Recommended Tools: Snort or Suricata
Both are open-source, industry-standard NIDS solutions with active communities and no licensing costs — ideal given budget constraints.

- **Snort:** Mature, widely documented, large rule community
- **Suricata:** Multi-threaded (better performance on modern hardware), supports both IDS and IPS modes if the organization later wants to upgrade

---

## How NIDS Addresses the Organization's Needs

| Concern | How NIDS Helps |
|---|---|
| Unauthorized access between segments | Monitors traffic at segment boundaries; alerts on policy violations |
| Limited IT staff | Alert-based system — team reviews alerts rather than configuring complex real-time blocking rules |
| OS/application vulnerability tracking | Traffic analysis reveals which OS versions and applications are communicating on the network |
| Encrypted malicious traffic | Signature-based detection can flag known malicious patterns even in partially encrypted flows |
| Data exfiltration risk | Monitors for unusual outbound data volumes or connections to unknown external IPs |

---

## Resource Requirements
- **Hardware:** Dedicated server (or VM) with sufficient CPU and storage to handle continuous traffic analysis across all 4 segments
- **Training:** 2 IT team members trained on NIDS installation, rule configuration, and alert triage
- **Maintenance:** Regular rule/signature updates to stay current with emerging threats

---

## Key Takeaway
NIDS is the right fit for this organization at this stage — it provides meaningful visibility and detection capability within the budget and staffing constraints, without the complexity of a full IPS deployment. As the team matures and budget grows, the NIDS foundation makes it easy to layer in additional controls or upgrade to active prevention.

---

## Skills Demonstrated
`NIDS vs IPS Analysis` `Snort` `Suricata` `Open-Source Security Tools` `Technology Evaluation` `Organizational Risk Assessment` `Financial Sector Security` `Network Segment Monitoring` `Security Recommendation Writing` `Least Privilege (Applied)`
