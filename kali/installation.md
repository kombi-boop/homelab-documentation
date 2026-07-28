# Kali Linux VM Installation

## Overview

This document covers the creation and configuration of the Kali Linux virtual machine running on Proxmox VE.

---

## Purpose

The Kali Linux VM will be used for:

- Cybersecurity learning
- Penetration testing practice
- Network analysis
- Security labs
- CTF environments

---

## VM Specifications

| Component | Configuration |
|-----------|---------------|
| Hypervisor | Proxmox VE |
| Operating System | Kali Linux |
| CPU | TBD |
| RAM | TBD |
| Storage | TBD |
| Network | vmbr0 |

---

## Installation

### ISO

- Kali Linux ISO downloaded from the official website.
- ISO uploaded to Proxmox storage.

### VM Creation

Configuration:

- Created new virtual machine.
- Attached Kali ISO.
- Configured CPU and memory.
- Added virtual disk.
- Connected network adapter to vmbr0.

---

## Initial Configuration

After installation:

- Updated system packages.
- Configured user account.
- Installed required tools.
- Verified network connectivity.

---

## Verification

Completed:

- Kali boots successfully.
- Network connectivity works.
- Proxmox console access works.

---

## Tools Installed

(To be updated)

---

## Lessons Learned

Problems encountered and solutions will be documented here.
