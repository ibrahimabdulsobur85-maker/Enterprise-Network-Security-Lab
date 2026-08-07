# Inter-VLAN Routing Testing

## Objective

The purpose of this test is to verify that devices in
different VLANs can communicate through the Company Router.

## Testing Method

ICMP ping was used to test connectivity between devices
located in different VLANs.

## Test Results

| Source | Destination | VLAN | Result |
|---|---|---:|---|
| HR-PC1 | Finance-PC1 | 10 → 20 | ✅ Successful |
| HR-PC1 | IT-PC1 | 10 → 30 | ✅ Successful |
| HR-PC1 | Server1 | 10 → 40 | ✅ Successful |

## Result

All tested VLANs were able to communicate successfully,
confirming that Inter-VLAN Routing is functioning correctly.

## Test Evidence

![Inter-VLAN Routing Test](inter-vlan-routing-test.png)
