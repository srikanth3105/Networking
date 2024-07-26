# OSPF Single Area Lab

## Overview
This lab involves configuring OSPF in a single area (Area 0) across three routers (R1, R2, and R3). Each router has an internal network connected to PCs through a switch, and they are interconnected via serial links.

## Learning Objectives
- Understand and configure OSPF in a single area.
- Learn how to set up and verify OSPF neighbor relationships.
- Practice configuring OSPF network types and advertising networks in OSPF.
- Gain experience in troubleshooting OSPF configurations and connectivity issues.

## Network Topology
- **Router 1 (R1)**: Connected to internal network `192.168.1.0/24` and Router 2.
- **Router 2 (R2)**: Connected to internal network `192.168.2.0/24`, Router 1, and Router 3.
- **Router 3 (R3)**: Connected to internal network `192.168.3.0/24` and Router 2.

### Network Addressing
- **R1 g0/0/1**: 192.168.1.100/24
- **R1 S0/0**: 10.0.0.1/30
- **R2 g0/0/1**: 192.168.2.100/24
- **R2 S0/0**: 10.0.0.2/30
- **R2 S0/1**: 11.0.0.1/30
- **R3 g0/0/1**: 192.168.3.100/24
- **R3 S0/0**: 11.0.0.2/30

## OSPF Configuration
The OSPF routing protocol is configured on all routers, with all interfaces participating in Area 0. Each router advertises its connected networks into OSPF.

### Configuration Summary
- **Router 1 (R1)**:
  - Internal Network: `192.168.1.0/24`
  - External Network: `10.0.0.0/30`
- **Router 2 (R2)**:
  - Internal Network: `192.168.2.0/24`
  - External Networks: `10.0.0.0/30`, `11.0.0.0/30`
- **Router 3 (R3)**:
  - Internal Network: `192.168.3.0/24`
  - External Network: `11.0.0.0/30`

## Steps to Implement
1. **Configure Router Hostnames and Interfaces**
2. **Enable OSPF and Advertise Networks**
3. **Verify OSPF Configuration**
   - Use commands like `show ip ospf neighbor` and `show ip route` to verify OSPF neighbor relationships and routing table entries.
4. **Test Connectivity**
   - Ensure that PCs in each subnet can communicate with each other across the network.

## Conclusion
This lab demonstrates the basic setup and configuration of OSPF in a single area, emphasizing the importance of correct IP addressing and OSPF area configuration for network stability and connectivity.
