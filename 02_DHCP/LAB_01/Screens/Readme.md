
# Packet Tracer DHCP Lab
## Objective
Configure a basic DHCP network in Packet Tracer. The router will act as the DHCP server and allocate IP addresses to a client PC.

## Topology
-** Router: ESR 4321
-** Switch: Multilayer switch (configured as a basic Layer 2 switch)
-** PC: PC0

## Configure DHCP on Router1 as follows
-** Excluded address range 10.1.1.1 to 10.1.1.100
** Pool name = pc
** Network 10.1.1.0/24
** Default Gateway = Router 1
** DNS Server = Router 1
** Test that PC can ping loopback of Router 1
