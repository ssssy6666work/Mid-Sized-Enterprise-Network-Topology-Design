# Implementation Checklist

## Phase 1: Network Preparation

- [ ] Confirm VLAN list.
- [ ] Confirm IP address plan.
- [ ] Configure VLAN interfaces.
- [ ] Configure DHCP scopes.
- [ ] Confirm routing between firewall and switches.
- [ ] Confirm internet access.

## Phase 2: Firewall Policy

- [ ] Create address objects.
- [ ] Create service objects.
- [ ] Configure deny-by-default inter-VLAN policy.
- [ ] Allow required business traffic.
- [ ] Block guest access to internal networks.
- [ ] Block user access to management network.
- [ ] Enable logging.

## Phase 3: Wireless

- [ ] Create Corp-WiFi SSID.
- [ ] Create Guest-WiFi SSID.
- [ ] Create IoT-WiFi SSID.
- [ ] Map each SSID to correct VLAN.
- [ ] Configure RADIUS authentication for Corp-WiFi.
- [ ] Test wireless access.

## Phase 4: VPN

- [ ] Configure IPsec VPN.
- [ ] Define HQ and branch subnets.
- [ ] Apply VPN firewall rules.
- [ ] Test branch access.
- [ ] Enable VPN logging.

## Phase 5: Validation

- [ ] Guest can access internet.
- [ ] Guest cannot access internal networks.
- [ ] Office PC can access required servers.
- [ ] Office PC cannot access management interfaces.
- [ ] CCTV can access NVR.
- [ ] CCTV cannot access internet by default.
- [ ] VPN user can access allowed services.
- [ ] Logs are generated correctly.
