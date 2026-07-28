# 🖥️ Homelab Documentation

> Documenting my journey building a modern homelab for virtualization, self-hosting, networking, Linux, and cybersecurity.

---

## 📖 About

This repository documents the development of my personal homelab from the ground up.

The goal is to create a practical environment for learning infrastructure, system administration, networking, and cybersecurity while documenting every step of the process.

Rather than only showcasing the finished result, this repository serves as an engineering journal that records the design decisions, successes, mistakes, and lessons learned throughout the project.

---

## 🎯 Objectives

- Learn Linux system administration
- Master Proxmox Virtual Environment
- Build a secure self-hosted infrastructure
- Practice networking concepts
- Develop cybersecurity skills
- Automate repetitive tasks
- Document everything for future reference

---

## 🖥️ Hardware

| Component | Specification |
|-----------|---------------|
| Host | Dell OptiPlex 3020 MT |
| CPU | Intel Core i5-4590 |
| RAM | 8 GB DDR3 *(planned upgrade to 16 GB)* |
| Storage | 120 GB SSD + 500 GB HDD |

---

## 🏗️ Planned Architecture

```
                    Internet
                        │
                   ISP Router
                        │
                  Proxmox VE Host
          ┌──────────┼──────────┐
          │          │          │
        Kali     Docker VM   Windows
                      │
      ┌───────────────┼────────────────┐
      │               │                │
   Jellyfin      AdGuard Home     Homepage
      │
  Sonarr / Radarr / Prowlarr
```

---

## 📁 Repository Structure

```
.
├── docs/
├── images/
├── kali/
├── proxmox/
├── scripts/
└── README.md
```

---

## 🚀 Roadmap

### Phase 1 — Foundation

- [x] Create GitHub repository
- [x] Configure Git with SSH
- [x] Initialize project structure
- [ ] Install Proxmox VE
- [ ] Configure storage
- [ ] Configure networking

### Phase 2 — Virtual Machines

- [ ] Kali Linux
- [ ] Windows VM
- [ ] Docker VM

### Phase 3 — Self-Hosted Services

- [ ] Jellyfin
- [ ] Sonarr
- [ ] Radarr
- [ ] Prowlarr
- [ ] Homepage
- [ ] AdGuard Home
- [ ] Uptime Kuma
- [ ] Nginx Proxy Manager

### Phase 4 — Cybersecurity Lab

- [ ] Active Directory Lab
- [ ] SIEM
- [ ] Vulnerable Machines
- [ ] CTF Practice
- [ ] Network Monitoring

---

## 📚 Documentation

| Section | Description |
|----------|-------------|
| `/proxmox` | Proxmox installation and configuration |
| `/kali` | Kali Linux setup and tools |
| `/docs` | Hardware, networking, architecture, troubleshooting |
| `/scripts` | Automation scripts |

---

## 📈 Project Status

🚧 Currently rebuilding the homelab from scratch.

Every major change, configuration, and lesson learned will be documented in this repository.

---

## 📜 License

This project is licensed under the MIT License.
