# Addressing Table

> Update this whenever you add a device, interface, subnet, or VLAN.

| Sites |
|-------|
| London |
| Paris |
| Madrid |

## Subnets / VLANs

| VLAN | Name | Subnet | Gateway | Purpose |
|------|------|--------|---------|---------|
| 10 | USERS | 10.0.10.0/24 | 10.0.10.1 | End-user hosts |
| 20 | SERVERS | 10.0.20.0/24 | 10.0.20.1 | Servers |
| 99 | MGMT | 10.0.99.0/24 | 10.0.99.1 | Device management |

## Interface assignments

| Device | Interface | IP / Mask | VLAN | Connects to |
|--------|-----------|-----------|------|-------------|
| R1 | Gi0/0 | 10.0.10.1 /24 | 10 | SW1 Gi0/1 (trunk) |
| R1 | Gi0/1 | 203.0.113.2 /30 | — | ISP / R2 |
| SW1 | VLAN99 | 10.0.99.2 /24 | 99 | — (mgmt SVI) |
| PC1 | NIC | 10.0.10.10 /24 | 10 | SW1 Fa0/2 |

## Routing
- **Protocol:** _OSPF area 0 / EIGRP AS 1 / static_
- **Notes:** _summarization, default route origination, etc._
