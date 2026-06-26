# Logging and Monitoring

## Purpose

This document defines basic log sources and monitoring use cases for the enterprise network security lab.

## Log Sources

| Source | Events to Monitor |
|---|---|
| Firewall | Denied traffic, IPS events, admin login, VPN status |
| Switches | Port status, configuration change, STP event |
| Wireless AP | Authentication failure, rogue AP, client connection |
| RADIUS | Login success/failure, rejected authentication |
| Servers | Failed login, privilege change, service failure |
| VPN | Tunnel up/down, login failure, unusual access |

## Basic Use Cases

| Use Case | Indicator | Action |
|---|---|---|
| Brute-force attempt | Many failed logins | Block source, reset password, review account |
| Port scanning | One source to many ports | Investigate host, block if needed |
| Guest-to-LAN attempt | Guest VLAN to private subnet | Confirm firewall block |
| Unauthorized admin access | Non-admin source to management VLAN | Investigate endpoint |
| Abnormal VPN access | Login from unusual time/location | Verify user identity |

## Daily Review Checklist

- [ ] Review critical firewall denies.
- [ ] Review VPN failures.
- [ ] Review RADIUS failures.
- [ ] Review admin login events.
- [ ] Check device availability.
- [ ] Escalate suspicious events.
