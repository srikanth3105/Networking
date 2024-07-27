# Standard Access Control List

## Tasks
### Configure the appropriate router as per rules given
  - Deny the host 192.168.1.1 communicating with 192.168.2.0
  - Deny the host 192.168.1.3 communicating with 192.168.2.0
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

