# Site-to-Site VPN Design

## Purpose

This document describes a sample IPsec site-to-site VPN design between HQ and a branch office.

## VPN Design

| Item | Value |
|---|---|
| VPN Type | IPsec Site-to-Site |
| IKE Version | IKEv2 |
| Encryption | AES-256 |
| Integrity | SHA-256 |
| Authentication | Pre-shared key or certificate |
| HQ subnet | 10.10.0.0/16 |
| Branch subnet | 10.20.0.0/16 |

## Security Controls

- Use strong encryption and integrity algorithms.
- Restrict branch traffic to required HQ services only.
- Do not allow branch users to access the management VLAN by default.
- Log tunnel up/down events.
- Log VPN negotiation failures.
- Rotate VPN secrets according to policy.
- Use certificate-based authentication if the environment supports it.

## Allowed Traffic Example

| Source | Destination | Service | Action |
|---|---|---|---|
| Branch LAN | HQ DNS | DNS | Allow |
| Branch LAN | HQ Application Server | HTTPS | Allow |
| Branch LAN | HQ File Server | SMB if required | Allow |
| Branch LAN | HQ Management VLAN | Any | Deny |
| HQ IT Admin | Branch firewall/switches | SSH/HTTPS | Allow |
