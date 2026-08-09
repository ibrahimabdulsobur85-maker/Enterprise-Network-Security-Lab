# BPDU Guard Configuration

## Objective

BPDU Guard is configured on end-device access ports to protect
the network from unauthorized switches or other devices that
send Bridge Protocol Data Units (BPDUs).

If a BPDU is received on a protected access port, the port is
placed into an error-disabled state.

## Configuration

On Switch0:

```cisco

### 1. Enable BPDU Guard on Access Ports

enable
configure terminal

interface range fa0/2-13
spanning-tree bpduguard enable
exit
