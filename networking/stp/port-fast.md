# PortFast Configuration

## Objective

PortFast is configured on end-device access ports to allow them
to transition directly to the forwarding state instead of going
through the normal STP listening and learning states.

This reduces the time required for end devices such as PCs and
servers to become operational after connecting to the network.

## Configuration

On Switch0:

```cisco

## Enable PortFast on Access Ports

enable
configure terminal

interface range fa0/2-13
spanning-tree portfast
exit
