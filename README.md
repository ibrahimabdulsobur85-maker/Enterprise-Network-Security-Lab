# Secure Small Office Network

## Project Overview

This project demonstrates the design, configuration, and security
of a small office network using Cisco networking technologies.

The network was designed with VLAN segmentation, inter-VLAN routing,
centralized DHCP, Layer 2 security controls, secure remote management,
NAT, ACLs, and WAN connectivity.

## Network Architecture

The network consists of:

- 1 Company Router
- 2 Switches
- Multiple PCs
- 1 Server
- 1 ISP Router

The network is divided into four departments using VLANs.

## VLAN Structure

| VLAN | Department | Network |
|------|------------|---------|
| 10 | HR | 192.168.10.0/24 |
| 20 | Finance | 192.168.20.0/24 |
| 30 | IT | 192.168.30.0/24 |
| 40 | Server | 192.168.40.0/24 |

VLAN segmentation separates the departments into different
broadcast domains and improves network organization and security.

## Technologies Implemented

### VLANs

Four VLANs were created to logically separate the departments
and server network.

### Inter-VLAN Routing

Router-on-a-Stick was configured to allow communication between
the VLANs where permitted.

### DHCP

The Company Router provides dynamic IP addressing to the internal
VLANs.

### DHCP Snooping

DHCP Snooping was implemented on the switches to help prevent
rogue DHCP servers from providing unauthorized network
configuration.

### Port Security

Port Security was configured on access ports with a maximum of
one secure MAC address.

Violation modes were configured according to the network design:

- VLAN 10 — Restrict
- VLAN 20 — Restrict
- VLAN 30 — Restrict
- VLAN 40 — Shutdown

Sticky MAC learning was used on the access ports.

### STP Security

PortFast was enabled on end-device access ports.

BPDU Guard was also configured to protect access ports from
unexpected BPDU frames.

### SSH

SSH was configured for secure remote management of the
Company Router.

SSH connectivity was successfully tested from a network PC.

### NAT

Network Address Translation was configured so that internal
private addresses can communicate through the Company's WAN
interface.

NAT overload allows multiple internal devices to share the
outside interface address.

### ACL

An extended ACL was configured to protect the Server VLAN.

Traffic from VLANs 10, 20, and 30 toward VLAN 40 was blocked,
while other traffic was permitted.

### WAN Connectivity

The Company Router was connected to an ISP Router to provide
external network connectivity.

## Security Controls

The project implements multiple layers of network security:

1. VLAN segmentation
2. DHCP Snooping
3. Port Security
4. PortFast
5. BPDU Guard
6. SSH management
7. ACL-based traffic filtering
8. NAT

These controls demonstrate a layered approach to securing a
small office network.

## Testing

The completed network was tested for:

- Inter-VLAN connectivity
- DHCP operation
- DHCP Snooping bindings
- Port Security
- STP security
- SSH connectivity
- NAT translations
- ACL enforcement
- WAN connectivity

The network successfully passed the final connectivity and
security tests.

Detailed evidence and configuration documentation can be found
in the individual project folders.

## Project Documentation

```text
project/
├── vlan/
├── inter-vlan/
├── dhcp/
├── wan/
├── default-route/
├── dhcp-snooping/
├── port-security/
├── portfast/
├── bpduguard/
├── ssh/
├── nat/
├── acl/
├── final-testing/
└── README.md
