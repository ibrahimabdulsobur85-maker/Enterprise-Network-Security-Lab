# Inter-VLAN Routing

## Objective

Inter-VLAN routing allows devices in different VLANs to
communicate through the Company Router.

The Company Router will use Router-on-a-Stick to provide
a default gateway for each VLAN.

## VLAN Gateway Addresses

| VLAN | Department | Gateway |
|------|------------|---------|
| 10 | HR | 192.168.10.1 |
| 20 | Finance | 192.168.20.1 |
| 30 | IT | 192.168.30.1 |
| 40 | Servers | 192.168.40.1 |

## Configuration
