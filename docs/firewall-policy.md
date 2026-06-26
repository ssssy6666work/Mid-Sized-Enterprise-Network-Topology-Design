# Firewall Policy Design

## Purpose

This document describes sample firewall policies for a segmented enterprise network.

## Policy Principles

- Deny by default between internal VLANs.
- Allow only required business traffic.
- Log denied traffic for investigation.
- Restrict management access to IT admin devices.
- Keep guest, IoT, and CCTV networks isolated.

## Sample Rule Table

| Priority | Source | Destination | Service | Action | Log | Description |
|---:|---|---|---|---|---|---|
| 1 | IT-Admin-PC | Management VLAN | SSH/HTTPS/SNMP | Allow | Yes | Admin access |
| 2 | Office-PC | Server VLAN | HTTPS/DNS/SMB as required | Allow | Yes | Business access |
| 3 | Office-PC | Management VLAN | Any | Deny | Yes | Prevent unauthorized admin access |
| 4 | Guest-WiFi | Internet | HTTP/HTTPS/DNS | Allow | Yes | Guest internet |
| 5 | Guest-WiFi | Internal RFC1918 | Any | Deny | Yes | Guest isolation |
| 6 | IoT | Internet | Required ports | Allow | Yes | IoT cloud access |
| 7 | IoT | Internal VLANs | Any | Deny | Yes | Prevent lateral movement |
| 8 | CCTV | NVR | Required camera ports | Allow | Yes | Recording traffic |
| 9 | CCTV | Internet | Any | Deny | Yes | Block camera internet access |
| 10 | VPN-Users | Server VLAN | Required services only | Allow | Yes | Remote work |
| 11 | Any | Firewall Management | Any | Deny | Yes | Protect firewall |

## Rule Review Process

- Review firewall rules every quarter.
- Remove unused rules.
- Confirm each allow rule has a business owner.
- Confirm broad allow rules are justified.
- Enable logging for high-risk denies and admin access.
