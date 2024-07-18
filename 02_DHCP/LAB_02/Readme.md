# Packet Tracer DHCP Lab
## Objective
Configure a basic DHCP network in Packet Tracer. The router will act as the DHCP server and allocate IP addresses to a client PC's.

## Topology
- Router: ESR 4321
- Switch: Multilayer switch (configured as a basic Layer 2 switch)
- PC: PC0
- PC: PC1

## Configure DHCP on Router1 as follows:
 1) Exclude first 10 IP addresses in each subnet from pool,
 2) Pool names = vlan10 and vlan20
 3) Networks =  10.1.10.0/24 (VLAN 10) and 10.1.20.0/24 (VLAN 20)
 4) Default Gateway = Switch1
 5) DNS Server = Router1
 6) Make sure PCs can ping each other and the loopback of Router1
 
## Before Engaging
- MLS is configured with VLANS, Vlan 10 -Gig 1/0/2 , Vlan 20 Gig 1/0/3
- SVI are configured on the switch
- Routing is not enabled on Switch
- 
