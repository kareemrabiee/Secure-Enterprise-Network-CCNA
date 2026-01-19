## Default Credentials – CCNA Network Lab

> **Important**
> All usernames and passwords here are **for learning only**.
> They are not real and should not be used in real networks.

---

## Routers (HQ, Branch, Cloud)

* Console password: `cisco`
* Enable password: `cisco`
* SSH username: `admin`
* SSH password: `Cisco123`

---

## Switches (HQ-SW1, HQ-SW2, BRANCH-SW)

* Console password: `cisco`
* Enable password: `cisco`
* SSH username: `admin`
* SSH password: `Cisco123`

---

## ISP Router

* Console password: `cisco`
* Enable password: `cisco`

SSH is not enabled on the ISP router.

---

## Management IPs

| Device    | IP Address   | VLAN |
| --------- | ------------ | ---- |
| HQ-SW1    | 192.168.99.2 | 99   |
| HQ-SW2    | 192.168.99.3 | 99   |
| BRANCH-SW | 192.168.99.4 | 99   |

---

## OSPF Authentication

* Type: MD5
* Key ID: 1
* Key: `secure-key`

---

## Quick Login

### Console

```
Router> enable
Password: cisco
Router#
```

### SSH

```
ssh admin@192.168.99.2
Password: Cisco123
```

---

## Notes

* In real networks, passwords must be stronger
* In real networks, AAA should be used
* This lab uses simple passwords to make learning easier

---

## For Learning Only

This lab is for CCNA practice and study only.
