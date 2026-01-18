# Secure Enterprise Network – Network Design Documentation

## 1. Project Overview
This document describes the design and implementation of a secure enterprise
network built using CCNA-level technologies.

The main objective of this project is to apply practical network security
concepts such as segmentation, access control, NAT, and secure routing
in a multi-site environment.

---

## 2. Business Scenario
The simulated company has the following requirements:

- A Headquarter (HQ) and a Branch office connected through a routed network
- Controlled and secure Internet access
- Guest users must be isolated from internal networks
- Public services must be accessible through a DMZ
- Secure connectivity to cloud-based services

---

## 3. Network Architecture

### Devices and Roles

| Device | Role |
|------|------|
| ISP-ROUTER | Internet service provider simulation |
| HQ-ROUTER | Core routing, NAT, and security enforcement |
| HQ-SW1 / HQ-SW2 | HQ access and distribution switches |
| BRANCH-ROUTER | Branch routing and security |
| BRANCH-SW | Branch access switch |
| CLOUD-ROUTER | Connectivity to cloud services |
| DMZ-SW | Switch for DMZ-hosted services |

---

## 4. VLAN Design

| VLAN | Purpose | Subnet |
|-----|--------|--------|
| 10 | HQ Users | 192.168.10.0/24 |
| 20 | HQ Servers | 192.168.20.0/24 |
| 30 | HQ Management | 192.168.30.0/24 |
| 40 | Guest Network | 192.168.40.0/24 |
| 50 | Branch Users | 172.16.50.0/24 |
| 60 | Branch Servers | 172.16.60.0/24 |
| 99 | Management VLAN | 192.168.99.0/24 |

VLANs are trunked between switches and routed using router-on-a-stick
at the HQ and Branch routers.

---

## 5. Security Design

### Access Control Lists (ACLs)
- Guest traffic is restricted to Internet access only.
- Internal users are allowed limited access based on role.
- Inbound Internet traffic is restricted to specific DMZ services.
- ACLs are applied inbound to stop unwanted traffic as early as possible.

### Network Address Translation (NAT)
- PAT is used for internal users accessing the Internet.
- Static NAT is configured for DMZ servers that require public access.

### Routing Security
- OSPF is used for dynamic routing across all sites.
- MD5 authentication is enabled on OSPF interfaces to prevent unauthorized routing updates.
- Passive interfaces are configured where appropriate.

### Device Management Security
- SSH version 2 is used for all remote management.
- VTY access is restricted using standard access lists.
- Local user authentication is configured on network devices.

### Layer 2 Security
- Port security is enabled on access ports.
- Sticky MAC addresses are used to limit unauthorized devices.

---

## 6. Verification and Testing

Verification was performed using standard IOS commands, including:

- `show vlan brief`
- `show interfaces trunk`
- `show port-security interface`
- `show access-lists`
- `show ip nat translations`
- `show ip ospf neighbor`
- `show ip ssh`

Screenshots for each verification step are included in the project repository.

---

## 7. Limitations and Future Improvements

- The design does not include advanced firewall technologies or IDS/IPS.
- Centralized logging and monitoring are not implemented.
- Future improvements may include:
  - Zone-Based Firewall
  - Syslog and SNMP monitoring
  - Cloud-native security controls (Security Groups, NACLs, IAM)

---

## 8. Conclusion
This project demonstrates how foundational network security concepts
can be applied in an enterprise-style topology using CCNA-level technologies.
It provides a solid base for transitioning to more advanced network
and cloud security architectures.
