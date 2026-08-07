# Enterprise Network Security Lab

## Project Overview

This project demonstrates the design, configuration, and
security of a small enterprise network using Cisco Packet Tracer.

The network simulates an organization with multiple departments,
an internal server network, Internet connectivity, network
segmentation, routing, DHCP, NAT/PAT, and security controls.

## Network Objectives

- Design an enterprise network topology
- Segment departments using VLANs
- Configure inter-VLAN routing
- Configure DHCP on the company router
- Configure an internal server network
- Configure Internet connectivity through an ISP router
- Configure NAT/PAT
- Implement ACLs
- Implement switch security
- Configure secure device management
- Test and troubleshoot network connectivity

## Network Architecture

The network consists of:

- ISP Router
- Company Router
- Core Switch
- HR Department
- Finance Department
- IT Department
- Internal Server

## VLAN Structure

| VLAN | Purpose | Network |
|------|---------|---------|
| 10 | HR | 192.168.10.0/24 |
| 20 | Finance | 192.168.20.0/24 |
| 30 | IT | 192.168.30.0/24 |
| 40 | Servers | 192.168.40.0/24 |

## IP Addressing

| Network | Default Gateway |
|---------|-----------------|
| 192.168.10.0/24 | 192.168.10.1 |
| 192.168.20.0/24 | 192.168.20.1 |
| 192.168.30.0/24 | 192.168.30.1 |
| 192.168.40.0/24 | 192.168.40.1 |

The Company Router will provide DHCP services for the
department VLANs.

The internal server will use a static IP address.

## Technologies

- Cisco Packet Tracer
- VLANs
- 802.1Q Trunking
- Inter-VLAN Routing
- DHCP
- NAT/PAT
- ACLs
- Port Security
- DHCP Snooping
- SSH

## Security Design

The network uses VLAN segmentation to separate departments
and the internal server network.

Access Control Lists (ACLs) will be used to control
communication between VLANs.

Additional switch security mechanisms will be implemented
to protect the network from unauthorized devices and
common Layer 2 attacks.

## Testing

The network will be tested for:

- VLAN connectivity
- Inter-VLAN routing
- DHCP address assignment
- Server connectivity
- Internet connectivity
- NAT/PAT functionality
- ACL enforcement
- Switch security

## Topology

The final network topology will be documented here.

## Author

Ibrahim Abdulsobur
