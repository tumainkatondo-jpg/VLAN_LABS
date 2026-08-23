# Network Topology Overview

This project demonstrates VLAN segmentation on a Cisco 2960-24TT switch using four PCs.

## Topology Summary
- VLAN 10: 192.168.10.0/24
  - PC0 → Fa0/1 → 192.168.10.3
  - PC1 → Fa0/2 → 192.168.10.2
- VLAN 20: 192.168.20.0/24
  - PC2 → Fa0/3 → 192.168.20.3
  - PC3 → Fa0/4 → 192.168.20.2

## Purpose
This setup isolates traffic between VLANs for better security and management. Devices in VLAN 10 cannot communicate directly with VLAN 20 unless routing is configured (e.g., via a Layer 3 switch or router-on-a-stick).

## How to Use
1. Load the configuration into the Cisco 2960 switch.
2. Assign IP addresses to PCs as shown.
3. Test connectivity:
   - Ping between PCs in the same VLAN (should succeed).
   - Ping between VLANs (should fail unless inter-VLAN routing is added).

## Notes
- Ensure each PC’s default gateway is configured if routing is later introduced.
- VLANs can be extended to other switches using trunk ports.
- This topology is ideal for small campus or departmental segmentation.

Author: Tumain  
Date: August 2026

