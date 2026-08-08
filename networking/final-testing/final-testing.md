# Final Network Testing

## Objective

The completed network was tested to confirm that the configured
networking and security features operate as intended.

## 1. Inter-VLAN Connectivity

Connectivity between permitted VLANs was tested.

### Tests

- VLAN 10 → VLAN 20: PASS
- VLAN 10 → VLAN 30: PASS
- VLAN 10 → VLAN 40: BLOCKED by ACL as intended

The successful tests confirmed that inter-VLAN routing is working
for permitted traffic.

## 2. ACL Verification

Traffic from VLAN 10 toward the Server VLAN (VLAN 40) was tested.

### Result

```text
Destination host unreachable
