# PC-Free — Multi-OS Browser-Based Virtual Machine Suite

Run Linux, Android, Windows, macOS, and iOS directly in your web browser using Docker, KVM acceleration, and GitHub Codespaces. Free, fast, zero-lag, and no local software or powerful hardware required.

[![GitHub stars](https://img.shields.io/github/stars/jephersonRD/pc-free?style=social)](https://github.com/jephersonRD/pc-free/stargazers)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=flat&logo=docker&logoColor=white)](https://www.docker.com/)

---

## What is PC-Free?

PC-Free is an open-source platform that turns your web browser into a full virtual machine workstation capable of streaming popular operating systems:

- 🪟 **Windows 10 / 11** (Port 8006 - noVNC / RDP)
- 🐧 **Linux Desktop (Ubuntu XFCE)** (Port 8007 - Web Desktop)
- 🤖 **Android OS (Redroid / Scrcpy)** (Port 8008 - Web Touch Interface)
- 🍏 **macOS** (Port 8009 - KVM macOS)
- 📱 **iOS Web Environment** (Port 8010 - Web Touch Simulator)

---

## Quick Start Guide

### 1️⃣ Launching via Docker Compose

Run all virtual machines simultaneously:

```bash
docker-compose up -d
```

Or run an individual operating system:

```bash
# Windows 10/11
docker-compose -f windows.yml up -d

# Linux Desktop
docker-compose -f linux.yml up -d

# Android OS
docker-compose -f android.yml up -d

# macOS
docker-compose -f macos.yml up -d

# iOS Environment
docker-compose -f ios.yml up -d
```

---

## Browser Machine Launcher Interface

Open `vm.html` or visit the hosted web page to switch between running operating system streams, launch full-screen views, and manage virtual machines.

---

## Zero-Lag Performance Tweaks

- **Hardware Acceleration:** Ensure `/dev/kvm` is enabled on Linux host or GitHub Codespace for full vCPU speed.
- **High FPS Web Streaming:** Shared memory `shm_size: 2gb` is configured across web containers for fluid 60fps interaction.

---

## License

Distributed under the MIT License. See `LICENSE` for details.
