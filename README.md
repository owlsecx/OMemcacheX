# 🦉 OMemcacheX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OMemcacheX** — Memcached & Varnish Cache Hardening Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Memcached & Varnish Cache configuration hardening auditor

---

## ✨ Features

- Offline, read-only Memcached + Varnish Cache auditor
- Memcached: memcached.conf, sysconfig OPTIONS, units, stats exports, SASL / sasldb / authfile, UDP amp.
- Varnish: DAEMON_OPTS, varnish.params, varnishd unit, admin CLI -T / -S secret / -j jail / -p params
- VCL: ACLs, PURGE/BAN, XFF spoofing, cookie/auth caching, httpoxy, pipe, header leaks, inline C
- Rules with severity / CWE / MITRE ATT&CK, grade A+…F
- TXT / MD / JSON / CSV / SARIF, --fail-on, --demo

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OMemcacheX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
