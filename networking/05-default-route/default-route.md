# Default Route Configuration

## Objective

The objective of this configuration is to configure a default
route on the Company Router so that traffic destined for unknown
networks is forwarded to the ISP Router.

## Configuration

### 1. Configure the Default Route

```cisco
On the Company Router:

enable
configure terminal

ip route 0.0.0.0 0.0.0.0 203.0.113.2

## Verify the default route

show ip route

## Test connectivity to the ISP

ping 203.0.113.2
