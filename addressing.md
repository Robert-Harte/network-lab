# Addressing Table

> Update this whenever you add a device, interface, subnet, or VLAN.

## Sites

| Sites | Branch |
|-------|--------|
| London | Main |
| Paris | Main |
| Madrid | Main |

## Subnets / VLANs

| VLAN | Name | Subnet | Gateway | Purpose |
|------|------|--------|---------|---------|
| 10 | USERS | 10.0.10.0/24 | 10.0.10.1 | End-user hosts |
| 20 | SERVERS | 10.0.20.0/24 | 10.0.20.1 | Servers |
| 99 | MGMT | 10.0.99.0/24 | 10.0.99.1 | Device management |

## Devices

| Device | Role | End Devices Type |
|--------|------|------------------|
| LondonR1 | Main router connecting the London office(s) to the outside networks. |
| LondonSW-C1 | Core switch for the London offices. |
| LondonSW-C2 | Core switch for the London offices. |
| LondonSWB1-C1 | Core switch for the London office - Branch1. |
| LondonSWB1-C2 | Core switch for the London office - Branch1. |
| LondonSWB1-A1 | Access switch for the London office - Branch1. | Users |
| LondonSWB1-A2 | Access switch for the London office - Branch1. | Users |
| LondonSWB1-A3 | Access switch for the London office - Branch1. | Users |
| LondonSWB1-A4 | Access switch for the London office - Branch1. | Servers |

## Interface assignments

| Device | Interface | IP / Mask | VLAN | Connects to |
|--------|-----------|-----------|------|-------------|
| LondonR1 | Gi0/0 | 10.0.10.1 /24 | 10 | SW1 Gi0/1 (trunk) |
| R1 | Gi0/1 | 203.0.113.2 /30 | — | ISP / R2 |
| LondonSW1 | VLAN99 | 10.0.99.2 /24 | 99 | — (mgmt SVI) |


## Routing
- **Protocol:** _OSPF area 0 / EIGRP AS 1 / static_
- **Notes:** _summarization, default route origination, etc._
