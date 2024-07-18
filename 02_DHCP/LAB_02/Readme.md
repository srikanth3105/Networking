

- Configure DHCP on Router1 as follows:
 1) Exclude first 10 IP addresses in each subnet from pool,
 2) Pool names = vlan10 and vlan20
 3) Networks =  10.1.10.0/24 (VLAN 10) and 10.1.20.0/24 (VLAN 20)
 4) Default Gateway = Switch1
 5) DNS Server = Router1
 6) Make sure PCs can ping each other and the loopback of Router1
 
