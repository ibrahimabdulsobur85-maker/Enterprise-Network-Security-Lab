# Network Topology

## Overview

This topology represents a small enterprise network designed
using Cisco Packet Tracer.

The network consists of an ISP router, a company router, a
central switch, four VLANs, departmental PCs, and an internal
server network.

## Network Devices

- 1 ISP Router
- 1 Company Router
- 1 Core/Access Switch
- 12 Departmental PCs
- 3 Internal Servers

## VLAN Structure

| VLAN | Department | Network |
|------|------------|---------|
| 10 | HR | 192.168.10.0/24 |
| 20 | Finance | 192.168.20.0/24 |
| 30 | IT | 192.168.30.0/24 |
| 40 | Servers | 192.168.40.0/24 |

## Network Flow

Internet traffic will enter through the ISP router and reach
the company network through the company router.

The company router will provide:

- Inter-VLAN routing
- DHCP services
- NAT/PAT
- Access control using ACLs
- A default route toward the ISP

The switch provides VLAN segmentation for the different
departments and the server network.

## Department Segmentation

### VLAN 10 — HR

Network:

`192.168.10.0/24`

### VLAN 20 — Finance

Network:

`192.168.20.0/24`

### VLAN 30 — IT

Network:

`192.168.30.0/24`

### VLAN 40 — Servers

Network:

`192.168.40.0/24`

## Security Design

VLAN segmentation is used to separate departments and the
server network.

ACLs will later be configured to control communication between
the different VLANs.

Additional Layer 2 security mechanisms will also be implemented.

## Topology Diagram

The topology diagram is stored in:

`topology.png`
