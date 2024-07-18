
# Packet Tracer DHCP Lab
## Objective
Configure a basic DHCP network in Packet Tracer. The router will act as the DHCP server and allocate IP addresses to a client PC.

## Topology
** Router: ESR 4321
** Switch: Multilayer switch (configured as a basic Layer 2 switch)
** PC: PC0

##Configure DHCP on Router1 as follows
**1) Excluded address range 10.1.1.1 to 10.1.1.100
**2) Pool name = pc
**3) Network 10.1.1.0/24
**4) Default Gateway = Router 1
**5) DNS Server = Router 1
**6) Test that PC can ping loopback of Router 1
