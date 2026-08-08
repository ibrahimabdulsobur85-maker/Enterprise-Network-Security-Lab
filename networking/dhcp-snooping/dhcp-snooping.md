# DHCP Snooping Configuration

## Objective

The objective of this configuration is to protect the network
against unauthorized DHCP servers by enabling DHCP Snooping on
the switch.

DHCP Snooping allows legitimate DHCP traffic from trusted ports
while blocking unauthorized DHCP server responses from untrusted
ports.

## Configuration



```cisco

## Enable DHCP Snooping Globally

On Switch0:

enable
configure terminal

ip dhcp snooping

## enabling dhcp snooping on the VLANs

ip dhcp cnooping vlan 10,20,30,40

## configure the roter facing port

int f0/1
ip dhcp snooping trust
exit

## configure dhcp rate limiting on access ports

int range f0/2-13
ip dhcp snooping rate limit 10
exit

## verification

show ip dhcp snooping
