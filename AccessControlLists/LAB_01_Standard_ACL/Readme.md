# Standard Access Control List

## Tasks
### Configure the appropriate router as per rules given
  - Deny the host 192.168.1.1 communicating with 192.168.2.0
  - Deny the host 192.168.1.2 communicating with 192.168.2.0
  - Deny the network 192.168.3.0 communicating with 192.168.3.0
  - Permit all remaining traffic
  - The above all rules should not affect the other communication
### Syntax for standard access-list
- Router(config)#access-list <ACLnumber> <permit/deny> <source_address> <source_wild_card_mask>
### To write ACL statement
- on which router to implement ACl
- Identify Source and Destination
- in/out
- Ensure the router you are implementing ACL must be a transit router
- Think your router as destination(incoming as source)

### Router 2 Config
R2#
R2#conf t
Enter configuration commands, one per line.  End with CNTL/Z.
R2(config)#access-list 2 deny 192.168.1.1 0.0.0.0
R2(config)#access-list 2 deny host 192.168.1.2
R2(config)#access-list 2 deny 192.168.3.0 0.0.0.255
R2(config)#access-list 2 permit any
R2(config)#exit
R2#
%SYS-5-CONFIG_I: Configured from console by console

R2#sh access-list?
access-lists  
R2#sh access-lists
Standard IP access list 2
    10 deny host 192.168.1.1
    20 deny host 192.168.1.2
    30 deny 192.168.3.0 0.0.0.255
    40 permit any
R2#
R2#conf t
Enter configuration commands, one per line.  End with CNTL/Z.
R2(config)#int g0/0/0
R2(config-if)#ip access
R2(config-if)#ip access-group ?
  <1-199>  IP access list (standard or extended)
  WORD     Access-list name
R2(config-if)#ip access-group 
% Incomplete command.
R2(config-if)#ip acc
R2(config-if)#ip access-group 2 out
R2(config-if)#exit
R2(config)#wr
