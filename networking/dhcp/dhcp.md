# DHCP Configuration

## Objective

The objective of this configuration is to configure the Company Router
as a DHCP server for the different VLANs in the organization.

The router automatically assigns IP addresses, subnet masks, and
default gateways to devices in each VLAN.

## DHCP Design

| VLAN | Department | Network | Default Gateway |
|------|------------|---------|-----------------|
| 10 | HR | 192.168.10.0/24 | 192.168.10.1 |
| 20 | FINANCE | 192.168.20.0/24 | 192.168.20.1 |
| 30 | IT | 192.168.30.0/24 | 192.168.30.1 |
| 40 | SERVERS | 192.168.40.0/24 | 192.168.40.1 |

## Configuration

### 1. Exclude Gateway Addresses

The default gateway addresses were excluded from the DHCP pools
to prevent the router from assigning its own gateway addresses
to client devices.

```cisco
ip dhcp excluded-address 192.168.10.1
ip dhcp excluded-address 192.168.20.1
ip dhcp excluded-address 192.168.30.1
ip dhcp excluded-address 192.168.40.1
