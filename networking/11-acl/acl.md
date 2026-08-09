# ACL Configuration

## Objective

An extended Access Control List (ACL) was configured on the
Company Router to protect the Server VLAN (VLAN 40).

The ACL prevents VLANs 10, 20, and 30 from initiating IP
traffic toward the Server VLAN while allowing other traffic
that is not specifically denied.

## Configuration


```cisco

## 1. Create the Extended ACL

ip access-list extended SERVER-PROTECTION

deny ip 192.168.10.0 0.0.0.255 192.168.40.0 0.0.0.255
deny ip 192.168.20.0 0.0.0.255 192.168.40.0 0.0.0.255
deny ip 192.168.30.0 0.0.0.255 192.168.40.0 0.0.0.255

permit ip any any
exit

## apply the ACL

int g0/1.10
ip access-group SERVER-PROTECTION out
exit

## Verification

show access-lists SERVER-PROTECTION
