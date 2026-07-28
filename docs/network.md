# Network

## Overview

This document describes the network topology and addressing used by the homelab.

As the lab grows, this document will be updated to reflect changes in infrastructure, services, and network segmentation.

---

# Physical Topology

```
                    Internet
                        │
                  ISP Router
                        │
        ┌───────────────┴───────────────┐
        │                               │
   Personal Devices              Proxmox Host
                                   │
                      ┌────────────┼────────────┐
                      │            │            │
                    Kali      Docker VM    Windows VM
```

---

# Network Information

| Setting | Value |
|----------|-------|
| LAN Network | 192.168.11.0/24 |
| Gateway | 192.168.11.1 |
| Router | ISP Router |
| DNS | Router (temporary) |

---

# Planned IP Addressing

| Device | Planned Address |
|----------|----------------|
| Proxmox Host | 192.168.11.10 |
| Docker VM | 192.168.11.20 |
| Kali Linux | DHCP |
| Windows VM | DHCP |

> Static addresses will be assigned only to infrastructure services. Client virtual machines may continue using DHCP unless a static address becomes necessary.

---

# Future Improvements

- Dedicated DNS server
- Reverse proxy
- Tailscale remote access
- VLAN segmentation
- Network monitoring
- Firewall hardening

---

# Notes

This network is intentionally kept simple during the initial stages of the project. Additional complexity will be introduced gradually as new services and security labs are deployed.
