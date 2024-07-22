# EIGRP Lab Configuration on Cisco Packet Tracer

## Lab Objectives
1. Configure EIGRP on multiple routers.
2. Establish EIGRP neighbor relationships.
3. Advertise and learn routes using EIGRP.
4. Verify EIGRP configuration and operation.

## Lab Topology
Create a topology with three routers and three PCs connected as follows:

- **Router1**: Interfaces connected to SW >PC1 and Router2.
- **Router2**: Interfaces connected to Router1, Router3, and SW >PC2.
- **Router3**: Interfaces connected to Router2 and SW >PC3.

## Step-by-Step Configuration

### Step 1: Set Up the Topology

1. **Add Devices**:
   - Drag and drop three routers (`Router0`, `Router1`, `Router2`) and three PCs onto the workspace.
   - Connect the routers with serial links or Ethernet cables.
   - Connect Switches, PC's 

2. **Assign IP Addresses**:

    - **Router1**:
      - `GigabitEthernet0/0`: 192.168.1.1/24 (connected to PC1)
      - `Serial0/1/0`: 10.0.0.1/30 (connected to Router2)
    
    - **Router2**:
      - `Serial0/1/0`: 10.0.0.2/30 (connected to Router1)
      - `Serial0/1/1`: 11.0.0.1/30 (connected to Router3)
      - `GigabitEthernet0/0`: 192.168.2.1/24 
    
    - **Router3**:
      - `Serial0/1/0`: 11.0.0.2/30 (connected to Router2)
      - `GigabitEthernet0/0`: 192.168.3.1/24 

    - **PCs**:
      - PC0: 192.168.1.11/24, Default Gateway: 192.168.1.1
      - PC1: 192.168.1.12/24, Default Gateway: 192.168.1.1
      - PC2: 192.168.2.11/24, Default Gateway: 192.168.2.1
      - PC3: 192.168.2.12/24, Default Gateway: 192.168.2.1
      - PC4: 192.168.3.11/24, Default Gateway: 192.168.3.1
      - PC4: 192.168.3.12/24, Default Gateway: 192.168.3.1
     
3. **Verify Connections on**:
   - **Router1**:**Router2**:**Router3**
   - Sh ip int br
   - sh ip eigrp neighbors
   - sh ip eigrp topology
   - sh ip route eigrp
   - sh ip dhcp binding
   - on pc's, test pinging other devices
   
