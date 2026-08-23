# VLAN Trunking Network Topology

## Overview
This topology demonstrates VLAN segmentation and trunking between two Cisco 2960 switches using IEEE 802.1Q encapsulation.

### Devices
- **Switch 1 (SW1)**: Cisco 2960-24TT
- **Switch 2 (SW2)**: Cisco 2960-24TT
- **PCs**:
  - VLAN 10: 192.168.10.0/24 → PC0, PC1, PC3
  - VLAN 30: 192.168.30.0/24 → PC2, PC4, PC5

### Connections
- SW1 Fa0/3 ↔ SW2 Fa0/3 → Trunk link (802.1Q)
- SW1 Fa0/1, Fa0/2 → VLAN 10
- SW1 Fa0/4 → VLAN 30
- SW2 Fa0/4 → VLAN 10
- SW2 Fa0/1, Fa0/2 → VLAN 30

## Purpose
This setup allows VLANs to span across multiple switches using trunking. Devices in the same VLAN can communicate even if connected to different switches.

## Testing
1. Ping between PCs in the same VLAN (e.g., PC0 ↔ PC1 ↔ PC3 for VLAN 10).
2. Ping between VLANs should fail unless inter-VLAN routing is configured.
3. Verify trunk status:
