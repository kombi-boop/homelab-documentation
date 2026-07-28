# Proxmox Storage Configuration

## Overview

This document describes the storage configuration of the Proxmox VE host.

The system uses the SSD for the Proxmox operating system and VM storage, while the HDD is used as additional storage for data.

---

## Physical Disks

| Device | Size | Purpose |
|--------|------|---------|
| SSD (`/dev/sdb`) | 119.2 GB | Proxmox installation and local storage |
| HDD (`/dev/sda`) | 465.8 GB | Additional storage |

---

## Proxmox Storage Pools

Current storage configuration:

| Name | Type | Purpose |
|------|------|---------|
| local | Directory | Proxmox system files, ISO images, backups |
| local-lvm | LVM-Thin | Virtual machine and container disks |
| HDD-Storage | Directory | Additional data storage |

---

## Storage Details

### local

Type:

```
Directory
```

Used for:

- ISO images
- Backups
- Templates
- Proxmox files

---

### local-lvm

Type:

```
LVM-Thin
```

Used for:

- Virtual machine disks
- Container root filesystems

---

### HDD-Storage

Type:

```
Directory
```

Mount point:

```
/mnt/hdd
```

Used for:

- Large files
- Media storage
- Additional data

---

## Design Decisions

The storage is separated into two devices:

- SSD for the operating system and virtual machine performance.
- HDD for larger data storage.

This provides better organization and prevents large data files from consuming the system disk.

---

## Current Status

Storage configuration verified successfully using:

```bash
pvesm status
```

All storage pools are active.
