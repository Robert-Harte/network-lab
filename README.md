# Network Lab

Documentation for my CCNA study/practice network.

## Goals

To create a network in Packet Tracer to practice configuring cisco devices. The network will look to mimic common topologies used in businesses today.

The network will contain some of the following:

- Multi-site network using WAN topology, using at least 3 sites.
- Practice inter-VLAN routing, ACLs, DHCP, NAT, SSH.
- Make use of routing protocol such as OSPF.

## Contents
| File / Folder | Purpose |
|---------------|---------|
| `topology.drawio` | Physical + logical network diagram (open with [draw.io](https://app.diagrams.net) / diagrams.net) |
| `addressing.md` | IP addressing, subnet, and VLAN table |
| `configs/` | Saved device running-configs (one file per device) |
| `changelog.md` | Dated log of what changed and why |

## Lab environment
- **Simulator/hardware:** Packet Tracer

## Conventions
- Hostnames: `LondonR1`, `LondonR2` for routers; `LondonSW1`, `LondonSW2` for switches.
- All passwords configured on each device will be set to **cisco**.
- Update `addressing.md` and `changelog.md` whenever the topology changes.
