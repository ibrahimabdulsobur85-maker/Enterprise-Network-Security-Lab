# Port Security Configuration

## Objective

The objective of this configuration is to secure the switch
access ports by limiting the number of MAC addresses that can
connect to each port.

Port Security helps prevent unauthorized devices from connecting
to the company's network through unused or unauthorized access ports.

## Configuration

On Switch0:

```cisco

## VLAN 10 - HR Department

enable
configure terminal

## VLAN 10 - HR Department

interface range fa0/11-13
switchport mode access
switchport port-security
switchport port-security maximum 1
switchport port-security mac-address sticky
switchport port-security violation restrict
exit

## VLAN 20 - FINANCE Department

interface range fa0/8-10
switchport mode access
switchport port-security
switchport port-security maximum 1
switchport port-security mac-address sticky
switchport port-security violation restrict
exit

## VLAN 30 - IT Department

interface range fa0/2-4
switchport mode access
switchport port-security
switchport port-security maximum 1
switchport port-security mac-address sticky
switchport port-security violation restrict
exit

## VLAN 40 - SERVERS

interface range fa0/5-7
switchport mode access
switchport port-security
switchport port-security maximum 1
switchport port-security mac-address sticky
switchport port-security violation shutdown
exit

## Verification

show port-security
show port-security address
