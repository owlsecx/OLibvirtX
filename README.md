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

Offline KVM/QEMU/libvirt hypervisor configuration & domain XML auditor

---

## ✨ Features

- Offline, read-only audit of libvirt daemon config (listen_tcp, auth_*, socket perms, TLS verification, mDNS advertisement, access_drivers, audit/logging)
- qemu.conf auditor — emulator user/group, capability clearing, security_driver, namespaces, seccomp, NBD/ VNC/SPICE TLS + listen + password (always masked)
- Domain XML auditor — sVirt seclabels, PCI/USB host passthrough vs vIOMMU, USB redirection, shareable disks & cache modes, image perms, VNC/SPICE exposure, bound serial consoles, macvtap, nwfilter filterref, RNG backends, memballoon, cloud-init secrets in cmdline/sysinfo, qemu:commandline passthrough args
- Storage pool, network, nwfilter and secret XML checks (secret values are never decrypted — masked)
- AppArmor / SELinux virt profile reference checks
- Hardened XML parsing — DOCTYPE / ENTITY refused
- CWE / MITRE ATT&CK / CIS-KVM mapping per rule
- Score + grade, min-severity filter, --fail-on gate
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Hardened templates, rule catalogue, --explain
- Self-test --demo (weak + hardened fixture trees)

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OLibvirtX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
