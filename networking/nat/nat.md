# NAT Configuration

## Objective

Network Address Translation (NAT) was configured on the Company
Router to allow internal private IP addresses from the company
VLANs to communicate through the WAN connection using the
Company Router's outside interface.

## Configuration


The Company Router uses G0/1 toward the internal network and
G0/0 toward the ISP.

```cisco

### 1. Configure NAT Inside and Outside Interfaces

interface g0/0
ip nat outside
exit

interface g0/1
ip nat inside
exit

interface g0/1.10
ip nat inside
exit

interface g0/1.20
ip nat inside
exit

interface g0/1.30
ip nat inside
exit

interface g0/1.40
ip nat inside
exit

## create NAT list

access-list 1 permit 192.168.10.0 0.0.0.255
access-list 1 permit 192.168.20.0 0.0.0.255
access-list 1 permit 192.168.30.0 0.0.0.255
access-list 1 permit 192.168.40.0 0.0.0.255

## configure NAT overload

ip nat inside source list 1 interface g0/0 overload

## verification

show running-config | include ip nat

show ip nat translations
