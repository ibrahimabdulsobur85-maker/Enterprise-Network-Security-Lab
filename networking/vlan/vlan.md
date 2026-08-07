# VLAN Configuration

## Objective

VLANs are used to logically separate the organization's
departments and server network.

This improves network organization, segmentation, and security.

## VLANs

| VLAN | Name | Department/Purpose |
|------|------|--------------------|
| 10 | HR | Human Resources |
| 20 | FINANCE | Finance Department |
| 30 | IT | IT Department |
| 40 | SERVERS | Internal Servers |

## Network Addressing

| VLAN | Network |
|------|---------|
| 10 | 192.168.10.0/24 |
| 20 | 192.168.20.0/24 |
| 30 | 192.168.30.0/24 |
| 40 | 192.168.40.0/24 |

## Switch Port Assignment

| Ports | VLAN | Purpose |
|-------|------|---------|
| Fa0/11–Fa0/13 | VLAN 10 | HR PCs |
| Fa0/8–Fa0/10 | VLAN 20 | Finance PCs |
| Fa0/2–Fa0/4 | VLAN 30 | IT PCs |
| Fa0/5–Fa0/7 | VLAN 40 | Servers |

## Configuration

```cisco
vlan 10
name HR
exit

vlan 20
name FINANCE
exit

vlan 30
name IT
exit

vlan 40
name SERVERS
exit

## Assign HR Ports

int range f0/11-13
switchport mode access
switchport access vlan 10
exit

## Assign Finance ports

int range f0/8-10
switchport mode access
switchport access vlan 20
exit

## Assign IT Ports

int range f0/2-4
switchport mode access
switchport access vlan 30
exit

## Assign Server ports

int range f0/5-7
switchport mode access
switchport access vlan 40
exit

## Verification
show vlan brief
