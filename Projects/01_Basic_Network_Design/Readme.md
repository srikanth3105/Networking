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

### Lets get Started as per requirements
- in cisco packet tracer add all the devices establish connections with cables and color code departments in different VLANS, and Label the name of department, VLAN, Ip address with subnet mask.
- Refer to network topology screenshot
  
#### Configurations

##### Switch
    - Create VLANS
        - VLAN 10, IT
        - VLAN 20 , FINANCE
        - VLAN 30 , CUSTOMER_SERVICE
    - Assign ports to Vlans
    - Create a trunk port for the interface connecting siwtch and router
    - Write Configuration

##### Router Config
   - Create Sub interfaces to int g0/0 with vlan for instance int g0/0.10
   - Assign Ip address to each sub interface
   - on sub interface implement encapsulation dot 1q with VLAN id
   - Make sure interface are up
 
   - Configure DHCP pool for each department
   - give department specifi default gateway
   - DNS-server same as Default gateway
   - Domain-name as "department_Name.com" in place ofdepartment name provide actual department name
   - write configuration
     
##### Wireless Access Point
   - on each access point Configure on port 1, with SSID and WPA2-PSK password 

##### On End Devices
   - On each pc, in ip config change static to dhcp for assign ip address automatically by DHCP
   - similarly on printers
   - on laptop
       - power off and and WPC300N module
       - Connect to wirless network based on department SSID and password
##### Test Connection from End devices
  - Ping from pc from one department other similarly from laptops
 
  
  
  
      
