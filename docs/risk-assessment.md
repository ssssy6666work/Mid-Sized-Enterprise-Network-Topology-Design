# Security Risk Assessment

## Risk Register

| ID | Asset | Threat | Weakness | Impact | Likelihood | Risk | Mitigation |
|---:|---|---|---|---|---:|---|---|
| 1 | Internal network | Lateral movement | Flat network | High | Medium | High | VLAN segmentation |
| 2 | Guest Wi-Fi | Unauthorized access | No isolation | High | Medium | High | Deny guest to LAN |
| 3 | IoT devices | Device compromise | Weak firmware | Medium | Medium | High | IoT VLAN and restricted access |
| 4 | CCTV | Camera exposure | Internet access allowed | Medium | Medium | High | Block CCTV internet by default |
| 5 | Firewall | Unauthorized admin access | Broad management access | High | Low-Medium | High | Management VLAN and allowlist |
| 6 | VPN | Credential compromise | No MFA/log review | High | Medium | High | MFA and monitoring |
| 7 | Logs | Missed incident | No central logging | Medium | Medium | Medium | Syslog/SIEM forwarding |

## Treatment Plan

- High risks should have mitigation plans and owners.
- Firewall rules should be reviewed regularly.
- Guest and IoT traffic should be isolated.
- Management access should be limited to IT admin devices.
- Logs should be reviewed and retained according to policy.
