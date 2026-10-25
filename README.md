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

OMemcacheX is an offline Memcached and Varnish Cache hardening auditor. It reviews Memcached flags/SASL/TLS/UDP amplification and Varnish daemon options, admin CLI, secrets, jail, and VCL ACL/PURGE/BAN issues. Findings include severity, CWE, and MITRE ATT&CK with grade and TXT/MD/JSON/CSV/SARIF export.

---

## ✨ Features

- Memcached: memcached.conf, sysconfig OPTIONS, units, stats exports, SASL/sasldb/authfile, UDP amplification
- Varnish: DAEMON_OPTS, varnish.params, varnishd unit, admin CLI `-T`/`-S` secret/`-j` jail/`-p` params
- VCL review: ACLs, PURGE/BAN, XFF spoofing, cookie/auth caching, httpoxy, pipe, header leaks, inline C
- Optional version hints for Memcached/Varnish CVE context
- Rule catalogue with `--list-rules` / `--explain`; hardened templates
- Multi-format export, secret masking, `--demo` and `--fail-on` / `--min-severity` gates

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OMemcacheX -c /etc/memcached.conf --scan
./OMemcacheX --root ./collected --type varnish -f json -o varnish.json
./OMemcacheX --demo --fail-on high
./OMemcacheX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
