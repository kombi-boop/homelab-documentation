# Proxmox Networking Configuration

## Overview

This document describes the network configuration of the Proxmox VE host.

Proxmox uses a Linux bridge (`vmbr0`) to provide network connectivity to virtual machines and containers.

---

## Network Topology

```
Internet
    |
ISP Router
    |
Physical NIC (nic0)
    |
vmbr0 Bridge
    |
Proxmox Host
    |
Virtual Machines / Containers
```

---

## Physical Interface

| Interface | Purpose |
|-----------|---------|
| nic0 | Physical Ethernet interface connected to the LAN |

---

## Linux Bridge

| Interface | Address |
|-----------|---------|
| vmbr0 | 192.168.11.140/24 |

The bridge is used by Proxmox to connect virtual machines and containers to the local network.

---

## Network Information

| Setting | Value |
|---------|-------|
| Network | 192.168.11.0/24 |
| Gateway | 192.168.11.1 |
| Proxmox IP | 192.168.11.140 |
| Interface | vmbr0 |

---

## Remote Access

Tailscale is configured on the Proxmox host for secure remote access.

Private Tailscale addressing is intentionally not published in this repository.

---

## Verification

Network configuration was verified using:

```bash
ip a
```

The following interfaces are active:

- Physical Ethernet interface (`nic0`)
- Proxmox bridge (`vmbr0`)
- Tailscale interface (`tailscale0`)

---

## Future Improvements

Planned networking improvements:

- VLAN segmentation
- Dedicated management network
- Firewall rules
- Internal DNS
- Network monitoring
