# Port Security Configuration

## Objective

The objective of this configuration is to secure the switch
access ports by limiting the number of MAC addresses that can
connect to each port.

Port Security helps prevent unauthorized devices from connecting
to the company's network through unused or unauthorized access ports.

## Configuration

### 1. Configure the Access Ports

On Switch0:

```cisco
enable
configure terminal

interface range fa0/2-13
switchport mode access
switchport port-security
switchport port-security maximum 1
switchport port-security mac-address sticky
switchport port-security violation restrict
exit
