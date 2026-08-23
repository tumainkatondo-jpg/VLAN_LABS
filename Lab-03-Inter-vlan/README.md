# Network Topology Project

## Overview
This project demonstrates a simple LAN setup using Cisco Packet Tracer. The topology includes:
- One router (Router0)
- One switch (Cisco 2960)
- Four PCs divided into two subnets

## Topology Summary
| Device | Interface | IP Address | Subnet | VLAN |
|---------|------------|-------------|---------|------|
| Router0 | Gig0/0.1 | 10.0.0.1 | 10.0.0.0/24 | VLAN 10 |
| Router0 | Gig0/0.2 | 20.0.0.1 | 20.0.0.0/24 | VLAN 20 |
| PC1 | Fa0 | 10.0.0.3 | 10.0.0.0/24 | VLAN 10 |
| PC2 | Fa0 | 10.0.0.4 | 10.0.0.0/24 | VLAN 10 |
| PC3 | Fa0 | 20.0.0.2 | 20.0.0.0/24 | VLAN 20 |
| PC4 | Fa0 | 20.0.0.3 | 20.0.0.0/24 | VLAN 20 |

## Purpose
The topology demonstrates:
- Basic IP addressing and subnetting
- VLAN segmentation for network isolation
- Router-on-a-stick configuration for inter-VLAN routing

## How to Use
1. Open the `.pkt` file in Cisco Packet Tracer.
2. Configure each PC with its respective IP and gateway.
3. Apply the router and switch configurations from `network_config.txt`.
4. Test connectivity using `ping` between PCs across VLANs.

## Expected Results
- PCs within the same VLAN can communicate directly.
- PCs across VLANs communicate through Router0.
- Proper routing and VLAN isolation are verified via successful ping tests.

---

**Author:** Tumain Katondo
Date August 2026