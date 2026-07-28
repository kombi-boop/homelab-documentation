# Network

## Overview

This document describes the network configuration of the homelab.

---

## Physical Network

Internet
↓
ISP Router
↓
Dell OptiPlex 3020 MT (Proxmox Host)

---

## LAN

| Setting | Value |
|---------|-------|
| Router IP | 192.168.11.1 |
| Subnet | 192.168.11.0/24 |
| Gateway | 192.168.11.1 |
| DNS | Router (will change later) |

---

## Planned Static Addresses

| Device | IP |
|---------|----|
| Proxmox | 192.168.11.10 |
| Docker VM | 192.168.11.20 |
| Kali VM | DHCP |
| Windows VM | DHCP |

---

## Future

- VLANs
- Reverse Proxy
- Tailscale
- Remote access
