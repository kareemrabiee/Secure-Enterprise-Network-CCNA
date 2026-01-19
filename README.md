# 🔒 Secure Enterprise Network (CCNA Lab)

## Overview
This project represents a hands-on enterprise network built while reviewing
CCNA concepts, with a focus on practical security, segmentation, and routing.

The topology simulates a small enterprise environment including:
- Headquarters
- Branch office
- DMZ
- Cloud connectivity
- Controlled Internet access

---

## Project Scope

- Multi-site enterprise topology
- Secure inter-VLAN communication
- Controlled user, guest, and server access
- Dynamic routing between sites

---

## Implemented Features

- VLAN segmentation for users, servers, guest, and management
- Extended ACLs enforcing least-privilege traffic rules
- OSPF routing with MD5 authentication
- NAT (PAT for internal users, Static NAT for DMZ services)
- SSH-only device management
- Port security on access switch ports

---

## Topology

![Network Topology](01-Topology/Enterprise-Topology.png)

---

## Verification

Configuration and behavior were verified using Cisco IOS commands and real
traffic testing, including:

- show vlan brief
- show interfaces trunk
- show port-security interface
- show access-lists
- show ip nat translations
- show ip ospf neighbor
- show ip ssh

Verification screenshots are available in the `03-Screenshots` directory.

---

## Lessons Learned

- Small ACL mistakes can completely break connectivity
- Planning traffic flow is more important than memorizing commands
- OSPF authentication adds an important security layer
- Verification is a critical part of any network deployment

---

## Limitations

- Advanced security features such as firewall zones, IDS/IPS, and centralized
  logging were not implemented due to the CCNA-level scope
- The focus is on foundational enterprise networking and security concepts

---

## Repository Structure
```
Secure-Enterprise-Network-CCNA/
├── 01-Topology/        # Network topology diagrams
├── 02-Configs/         # Router and switch configurations
├── 03-Screenshots/     # Verification outputs
├── 04-Documentation/   # Network design notes
├── 05-PacketTracer-Lab # Packet Tracer lab file
└── README.md
```
---

## Notes

This project was built as part of CCNA review and hands-on practice.
It reflects real configuration challenges encountered during implementation.

---

## License

MIT License
