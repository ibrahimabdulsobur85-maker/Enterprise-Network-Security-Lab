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

```cisco

## Configure the Switch Trunk

int f0/1
switchport mode trunk
no shutdown
exit

## Enable the Router's inside interface

int g0/1
no shutdown
exit

## configure VLAN 10 Subinterface

int g0/1.10
encapsulation dot1q 10
ip address 192.168.10.1 255.255.255.0
exit

## configure VLAN 20 Subinterface

int g0/1.20
encapsulation dot1q 20
ip address 192.168.20.1 255.255.255.0
exit

##configure VLAN 30 Subinterface

int g0/0.30
encapsulation dot1q 30
ip address 192.168.30.1 255.255.255.0
exit

## configure VLAN 40 Subinterface

int g0/1.40
encapsulation dot1q 40
ip address 192.168.40.1 255.255.255.0
exit

## verification

show ip int brief
