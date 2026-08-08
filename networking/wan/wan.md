# WAN Configuration

## Objective

The objective of this configuration is to establish a WAN
connection between the Company Router and the ISP Router.

The WAN connection provides a path from the organization's
internal network toward the ISP/Internet.

## WAN Addressing

| Device | Interface | IP Address | Subnet Mask | Role |
|---|---|---|---|---|
| Company Router | G0/0 | 203.0.113.2 | 255.255.255.252 | WAN interface |
| ISP Router | G0/0 | 203.0.113.1 | 255.255.255.252 | ISP interface |

## Configuration

```cisco

## 1. Configure the Company Router WAN Interface


enable
configure terminal

interface g0/0
ip address 203.0.113.1 255.255.255.252
no shutdown
exit

## 2. Configure the ISP Roter WAN Interface

enable
configure terminal

interface g0/0
ip address 203.0.113.2 255.255.255.252
no shutdown
exit

## 3. Verify the interfaces

## On the comapny router

show ip int brief

## On the ISP router

show ip int brief

## 4. Test the WAN Connection

## From the company router

ping 203.0.113.2

## From the ISP Router 

ping 203.0.113.1
