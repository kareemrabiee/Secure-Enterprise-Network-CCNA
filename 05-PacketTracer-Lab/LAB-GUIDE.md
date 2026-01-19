## CCNA Enterprise Network Lab – Complete Guide

---

## Lab Overview

This Packet Tracer lab simulates a secure enterprise network with:

* Multiple sites
* VLAN segmentation
* OSPF routing
* Basic security controls

The goal is to practice real CCNA networking concepts in a simple and clear way.

---

## How to Use This Lab

### For Beginners

1. Open `enterprise-network-lab.pkt` in Packet Tracer
2. Use the login details from `CREDENTIALS.md`
3. Start testing from **Admin-PC (192.168.10.10)**

---

### For CCNA Students

1. Review the network design in `04-Documentation/`
2. Check device configs in `02-Configs/`
3. Try rebuilding the lab from scratch for practice

---

## Lab Verification Checklist

### Basic Tests

* Ping from **Admin-PC** to **HQ-Router (192.168.10.1)**
* Ping from **User-PC** to the Internet (**8.8.8.8**)
* SSH from **Admin-PC** to **HQ-SW1 (192.168.99.2)**

---

### Advanced Tests

* Check OSPF neighbors

  ```
  show ip ospf neighbor
  ```
* Check NAT translations

  ```
  show ip nat translations
  ```
* Test ACL behavior using different traffic types

---

## Troubleshooting Guide

### If Ping Does Not Work

1. Check IP address and gateway
2. Verify VLAN assignment
3. Review ACL rules

---

### If OSPF Is Not Working

1. Check OSPF network commands
2. Verify MD5 authentication settings
3. Make sure interfaces are up

---

## Learning Objectives

After completing this lab, you will understand:

* Basic enterprise network design
* VLAN configuration and trunking
* OSPF routing with authentication
* ACLs for traffic control
* NAT (PAT and Static)
* Secure access using SSH and port security

---

## Next Steps

To continue learning, try the following:

1. Change ACL rules and test the result
2. Add a new VLAN and update routing
3. Enable IPv6 and test connectivity
4. Add firewall rules for extra security

---

**Happy Learning!**
👍
