# 🦉 OLibvirtX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OLibvirtX** — KVM / QEMU / libvirt Hypervisor Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OLibvirtX is an offline KVM/QEMU/libvirt hypervisor auditor. It reviews `libvirtd.conf`, `qemu.conf`, domain/storage/network/nwfilter/secret XML, and AppArmor/SELinux virt profile references. Secrets are masked; findings map to CWE, MITRE ATT&CK, and CIS-KVM with score/grade and multi-format export.

---

## ✨ Features

- libvirtd.conf audit: listen_tcp, auth_*, socket perms, TLS verification, mDNS, access_drivers, audit/logging
- qemu.conf review: emulator user/group, capability clearing, security_driver, namespaces, seccomp, NBD/VNC/SPICE TLS
- Domain XML checks: sVirt labels, PCI/USB passthrough, shareable disks, VNC/SPICE exposure, nwfilter, cloud-init secrets
- Storage pool, network, nwfilter, and secret XML checks (secret values never decrypted)
- AppArmor/SELinux virt profile references; hardened XML parsing (DOCTYPE/ENTITY refused)
- Score/grade, templates, rule catalogue, TXT/MD/JSON/CSV/SARIF export, `--demo` and fail-on gates

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OLibvirtX --scan
./OLibvirtX --domain guest.xml --libvirtd libvirtd.conf --format json -o libvirt.json
./OLibvirtX --demo --fail-on high
./OLibvirtX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
