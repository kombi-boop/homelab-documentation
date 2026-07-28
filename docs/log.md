# Lab Journal

This file records the progress and major changes made during the development of the homelab.

---

# 2026-07-28

## Repository Initialization

Started rebuilding the homelab documentation from scratch.

Completed:

- Created GitHub repository
- Configured Git SSH authentication
- Created repository structure
- Added initial README
- Added project documentation folders

---

## Hardware Documentation

Documented the physical server hardware:

- Dell OptiPlex 3020 MT
- Intel Core i5-4590
- 8 GB DDR3 RAM
- 120 GB SSD
- 500 GB HDD

---

## Proxmox VE Deployment

Documented the Proxmox VE installation.

Completed:

- Installed Proxmox VE 9.2.5
- Configured SSD as the Proxmox system disk
- Configured HDD as additional storage
- Verified storage pools
- Verified network connectivity

---

## Storage Configuration

Documented Proxmox storage:

- local directory storage
- local-lvm LVM-thin storage
- HDD-Storage directory storage

The storage design separates the operating system and virtual machine storage from larger data storage.

---

## Networking Configuration

Documented the Proxmox network setup:

- Physical interface: nic0
- Linux bridge: vmbr0
- Proxmox address: 192.168.11.140/24
- Tailscale configured for remote access

---

## Current Status

The base virtualization platform is operational.

Next steps:

- Create Kali Linux virtual machine
- Document VM configuration
- Begin cybersecurity lab setup
