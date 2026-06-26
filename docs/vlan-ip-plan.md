# VLAN and IP Address Plan

## Purpose

This document defines the VLAN segmentation and IP address plan for the enterprise network security lab.

## VLAN Table

| VLAN ID | VLAN Name | Subnet | Gateway | DHCP Range | Purpose |
|---:|---|---|---|---|---|
| 10 | Office-PC | 10.10.10.0/24 | 10.10.10.1 | 10.10.10.50-10.10.10.200 | Employee computers |
| 20 | Server | 10.10.20.0/24 | 10.10.20.1 | Static IP preferred | Internal servers |
| 30 | Guest-WiFi | 10.10.30.0/24 | 10.10.30.1 | 10.10.30.50-10.10.30.230 | Guest internet |
| 40 | IoT | 10.10.40.0/24 | 10.10.40.1 | 10.10.40.50-10.10.40.200 | IoT devices |
| 50 | CCTV | 10.10.50.0/24 | 10.10.50.1 | 10.10.50.50-10.10.50.200 | Cameras and NVR |
| 60 | Management | 10.10.60.0/24 | 10.10.60.1 | Static IP preferred | Device management |
| 70 | VPN-Users | 10.10.70.0/24 | 10.10.70.1 | VPN pool | Remote access |
| 80 | DMZ | 10.10.80.0/24 | 10.10.80.1 | Static IP preferred | Isolated services |

## Design Notes

- Guest Wi-Fi is isolated from all internal private networks.
- Management VLAN is accessible only by IT admin devices.
- CCTV cameras should only communicate with the NVR.
- IoT devices should not initiate connections to internal servers unless required.
- Server VLAN should only expose required business services.
