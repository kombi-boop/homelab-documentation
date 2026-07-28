# Proxmox VE Installation

## Overview

This document covers the installation and initial configuration of the Proxmox VE host used for this homelab.

---

## Objective

Build a stable virtualization platform capable of hosting:

- Linux virtual machines
- Windows virtual machines
- Docker workloads
- Cybersecurity labs
- Self-hosted services

---

## Hardware

| Component | Specification |
| --------- | ------------- |
| Model | Dell OptiPlex 3020 MT |
| CPU | Intel Core i5-4590 |
| RAM | 8 GB DDR3 |
| OS Disk | 120 GB SSD |
| Data Disk | 500 GB HDD |


## Proxmox Version

| Component | Version |
|-----------|---------|
| Proxmox VE | 9.2.5 |
| Kernel | 7.0.14-6-pve |
---

## Installation Steps

### Download

- Downloaded the latest Proxmox VE ISO.

### Boot Media

- Created a bootable USB drive.

### BIOS

- Enabled virtualization (Intel VT-x).
- Configured the boot order.

### Installation

Proxmox VE was installed on the 120 GB SSD.

The storage layout was configured as follows:

- SSD (`sdb`) → Proxmox operating system and local VM storage
- HDD (`sda`) → Additional storage mounted at `/mnt/hdd`

The system was configured with:

- EFI boot partition
- LVM storage
- Linux bridge networking (`vmbr0`)
---

## Initial Configuration

- Updated package repositories.
- Installed available updates.
- Verified network connectivity.


## Storage Configuration

Current disks:

| Device | Size | Purpose |
|--------|------|---------|
| `/dev/sdb` | 119.2 GB | Proxmox system disk |
| `/dev/sda` | 465.8 GB | Additional HDD storage |

The HDD is mounted at: /mnt/hdd

---

## Verification

Completed:

- Proxmox web interface accessible
- SSH access working
- Network connectivity confirmed
- Storage disks detected correctly
- Tailscale configured for remote access

Current network:

| Interface | Address |
|-----------|---------|
| vmbr0 | 192.168.11.140/24 |
| tailscale0 | 100.x.x.x |
---

## Lessons Learned

This section will document any issues encountered during installation and how they were resolved.
