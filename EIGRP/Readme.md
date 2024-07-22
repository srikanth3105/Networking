# EIGRP Lab Configuration on Cisco Packet Tracer

## Lab Objectives
1. Configure EIGRP on multiple routers.
2. Establish EIGRP neighbor relationships.
3. Advertise and learn routes using EIGRP.
4. Verify EIGRP configuration and operation.

## Lab Topology
Create a topology with three routers and three PCs connected as follows:

- **Router1**: Interfaces connected to PC1 and Router2.
- **Router2**: Interfaces connected to Router1, Router3, and PC2.
- **Router3**: Interfaces connected to Router2 and PC3.

## Step-by-Step Configuration

### Step 1: Set Up the Topology

1. **Add Devices**:
   - Drag and drop three routers (`Router0`, `Router1`, `Router2`) and three PCs onto the workspace.
   - Connect the routers with serial links or Ethernet cables.
   - Connect each PC to its respective router with an Ethernet cable.

2. **Assign IP Addresses**:

    - **Router1**:
      - `GigabitEthernet0/0`: 192.168.1.1/24 (connected to PC1)
      - `Serial0/0/0`: 10.0.0.1/30 (connected to Router2)
    
    - **Router2**:
      - `Serial0/0/0`: 10.0.0.2/30 (connected to Router1)
      - `Serial0/0/1`: 10.0.0.5/30 (connected to Router3)
      - `GigabitEthernet0/0`: 192.168.2.1/24 (connected to PC2)
    
    - **Router3**:
      - `Serial0/0/1`: 10.0.0.6/30 (connected to Router2)
      - `GigabitEthernet0/0`: 192.168.3.1/24 (connected to PC3)

    - **PCs**:
      - PC1: 192.168.1.2/24, Default Gateway: 192.168.1.1
      - PC2: 192.168.2.2/24, Default Gateway: 192.168.2.1
      - PC3: 192.168.3.2/24, Default Gateway: 192.168.3.1
