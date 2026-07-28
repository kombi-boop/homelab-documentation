# LXC Container Strategy

## Overview

This document describes how Linux Containers (LXC) are used in the homelab.

LXC containers are preferred for lightweight services because they consume fewer resources than full virtual machines.

---

## Planned Containers

| Container | Purpose |
|-----------|---------|
| Jellyfin | Media server |
| Samba | Network file sharing |
| AdGuard Home | DNS filtering |
| Uptime Kuma | Service monitoring |
| Homepage | Dashboard |

---

## Container Design

Each service will run in its own container.

Benefits:

- Easier troubleshooting
- Better isolation
- Lower resource usage
- Simple backups

---

## Storage

Large data services will use the HDD storage.

Examples:

- Media files
- Backups
- Shared files
