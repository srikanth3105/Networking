# Branch Network Design
## Goal
Design and implement a standalone network for a branch office with one router and one switch. The network will support three departments, each on a separate VLAN, with wireless network access and automatic IP address assignment.
## Requirements
- Router and Switch: Deploy a single router and a single switch.
- Departments: Include IT, Finance, and Customer Service departments.
- VLANs: Assign each department to a separate VLAN.
- Wireless Network: Provide wireless access for all departments.
- IP Addressing: Configure DHCP to automatically assign IP addresses to all devices.
- Inter-department Communication: Ensure seamless communication between devices across all departments.
- Devices: At least two PCs, one laptop per department, and a Printer.
- Connectivity Testing: Verify connectivity between all devices using ping tests to ensure that all devices can communicate with each other.

# Lets get Started

## 1. Gather Information
- **Locations**: Single branch office.
- **Departments**: IT, Finance, and Customer Service.
- **Number of Devices**: Estimate the number of devices per department for wireless access point planning.
- **Existing Infrastructure**: Ensure compatibility with existing network hardware and software.

## 2. Design Network Topology
- **Network Diagram**: Create a diagram illustrating how the router, switch, VLANs, and wireless access points are interconnected.
  - **Router**: Connects to the switch and manages inter-VLAN routing.
  - **Switch**: Connects all VLANs and devices.
  - **Wireless Access Points**: Provide wireless connectivity for each department.
- **Topology Layout**:
  - **Router**: One router, connected to the switch.
  - **Switch**: Connects to all departments and wireless access points.
  - **Wireless Access Points**: Positioned to cover the entire area of each department.

## 3. Develop IP Addressing Scheme
- **Base Network**: 192.168.1.0/24
  - **IT VLAN**: 192.168.1.0/26 (supports up to 62 devices)
  - **Finance VLAN**: 192.168.1.64/26 (supports up to 62 devices)
  - **Customer Service VLAN**: 192.168.1.128/26 (supports up to 62 devices)
- **Subnet Mask**: 255.255.255.192
- **Gateway IPs**:
  - **IT VLAN**: 192.168.1.1
  - **Finance VLAN**: 192.168.1.65
  - **Customer Service VLAN**: 192.168.1.129
- **DHCP Pools**:
  - **IT VLAN**: 192.168.1.2 - 192.168.1.62
  - **Finance VLAN**: 192.168.1.66 - 192.168.1.126
  - **Customer Service VLAN**: 192.168.1.130 - 192.168.1.190

## 4. Hardware and Software Selection
- **Router**: Should support VLANs and inter-VLAN routing.
- **Switch**: Must support VLANs, trunking, and sufficient port capacity.
- **Wireless Access Points**: Ensure they support VLAN tagging and provide adequate coverage.

## 5. Configuration Plan
1. **Switch Configuration**:
   - Create VLANs for IT, Finance, and Customer Service.
   - Assign switch ports to the appropriate VLANs.
   - Configure trunking to the router for inter-VLAN traffic.
2. **Router Configuration**:
   - Set up sub-interfaces for each VLAN.
   - Configure DHCP pools for each VLAN.
   - Implement inter-VLAN routing to enable communication between VLANs.
3. **Wireless Access Points Configuration**:
   - Set up SSIDs and assign each SSID to the corresponding VLAN.
   - Configure security settings for wireless networks.

## 6. Implementation Plan
- **Hardware Installation**: Install and connect the router, switch, and wireless access points.
- **Configuration**:
  - Apply switch and router configurations.
  - Set up DHCP pools and VLANs.
  - Configure wireless access points with appropriate SSIDs and VLAN settings.
- **Testing**:
  - Verify connectivity between VLANs.
  - Test DHCP functionality for automatic IP assignment.
  - Ensure wireless access points are functioning and providing coverage.

## 7. Documentation
- **Network Diagram**: Update with final configurations and device placements.
- **Configuration Files**: Save and document router and switch configurations.
- **IP Addressing Scheme**: Document IP ranges, subnet masks, and gateway IPs.
- **Wireless Setup**: Record SSID, VLAN assignments, and security settings.


 
  
  
  
      
