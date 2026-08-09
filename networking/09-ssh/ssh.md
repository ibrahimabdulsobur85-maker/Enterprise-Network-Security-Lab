# SSH Configuration

## Objective

SSH (Secure Shell) was configured on the Company Router to provide
secure remote management of the network device.

SSH was used instead of Telnet because SSH encrypts the remote
management session.

## Configuration

```cisco

## Configure the Router Hostname

hostname COMPANY-ROUTER

## Configure the domain nmae

ip domain-name company.local

## Create a local user

username admin privilege 15 secret Admin@123

## Generate RSA keys

crypto key generate rsa

## Enable SSH version 2

ip ssh version 2

## configure the vty line

line vty 0 4
login local
transport input ssh
exit

## verification

show ip ssh
