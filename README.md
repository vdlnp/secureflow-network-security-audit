# SecureFlow Enterprise Network Security Audit & Hardening Plan

**Course:** CCS6224 — Network Security
**Program:** Bachelor of Degree in Computer Science, Faculty of Computing and Informatics, Multimedia University
**Group 5**

## Overview

This project is a simulated enterprise network security audit and hardening plan for **SecureFlow Sdn. Bhd.**, a fictional fintech company based in Cyberjaya, Malaysia. The assignment covers threat assessment using the STRIDE framework, a segmented enterprise network built in Cisco Packet Tracer, and an evaluation of key security protocols (TLS 1.3, SPF/DKIM/DMARC, IPsec vs TLS VPN).

## Contents

- **[docs/Network_Security_Group_5.pdf](docs/Network_Security_Group_5.pdf)** — full written report
- **screenshots/** — CLI and configuration evidence from Packet Tracer, organized by network zone
- **packet-tracer/** — the `.pkt` topology file (if included)

## Report Structure

1. Executive Summary
2. Scope and Methodology
3. Threat Assessment Findings (Passive, Active, Layer 2, Wireless, Application-layer attacks — STRIDE-mapped)
4. Network Architecture and Hardening Evidence
   - Internet Zone
   - DMZ Zone
   - Internal LAN Zone (VLAN segmentation, HSRP, Rapid-PVST)
   - Guest Wireless Zone
   - Branch Office Zone (OSPF, site-to-site IPsec)
   - Cross-Zone Security and High Availability
5. Security Protocol Evaluation
   - TLS 1.2 vs TLS 1.3
   - SPF, DKIM, DMARC
   - IPsec VPN vs TLS VPN
6. Consolidated Recommendations & Roadmap
7. Conclusion
8. References

## Network Architecture Summary

The topology uses a defence-in-depth design split into four trust zones:

| Zone | Trust Level | Key Components |
|---|---|---|
| Internet Zone | 0 (Untrusted) | ISP-CORE router, DSL modem, external validation host |
| DMZ Zone | 1 (Semi-Trusted) | Dual firewalls (FW1/FW2), dual web/DNS servers, IDS placeholders |
| Internal LAN Zone | 2 (Trusted) | VLANs 10/20/30/40/99/999, dual Layer 3 core switches with HSRP |
| Branch Office Zone | 2 (Trusted) | Dual edge routers, OSPF, site-to-site IPsec VPN over dual WANs |

## Team

| Student ID | Name |
|---|---|
| 253UC256V0 | Muhammad Nabil Haziq Bin Ahmad Jefry |
| 253UC256X4 | Viandra Lika Nur Prastya |
| 253UC256QP | Lim Guan Yee |
| 242UC244Q1 | Muhammad Aref bin Mohd Hasni |

## License

Coursework submitted for CCS6224, Multimedia University. Not licensed for reuse without permission from the authors.
