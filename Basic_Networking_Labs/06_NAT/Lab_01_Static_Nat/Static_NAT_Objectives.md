# Static NAT Configuration Lab

## Overview

In this lab, you will configure Static NAT on a router to allow external devices to access internal servers. This involves mapping a public IP address to an internal IP address and setting up DNS resolution to facilitate access to these servers.

## Objectives

### Configure the network as follows 
1) Router details: Outside = 8.8.8.100/24 ,Inside = 10.1.1.254/24, Default Route to 8.8.8.8
2) Configure static NAT so that the outside PC can access the internal HTTP, FTP and TFTP servers.
3) HTTP = 8.8.8.200 (NAT only the required port). DNS = myhttp.com
4) FTP = 8.8.8.201 (full static NAT). DNS = myftp.com
5) Verify that both the inside and the outside PCs can access the internal servers.
6) Inside host to use internal IP addresses
7) Outside host to use DNS names
## Network Topology

### Outside Network (Internet)

- Client PC: Accesses the internal servers via the public IP addresses.
- DNS Server: Resolves domain names to public IP addresses.

### Internal Network

- HTTP Server: Internal IP `10.1.1.100`
- FTP Server: Internal IP `10.1.1.101`
- Router Configured with public IP addresses and handles NAT.
- Inside PC: Can access internal servers directly using internal IP addresses.


## Testing and Verification

1. Verify External Access: Ensure that the outside client can access internal servers using public IPs.
2. Verify Internal Access: Ensure that internal PCs can access servers using internal IPs.
3. Test DNS Resolution: Confirm that domain names correctly map to the public IP addresses.
