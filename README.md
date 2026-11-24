# 🦉 OMemcacheX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
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

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OMemcacheX --help   # watch every network call
firejail --net=none ./OMemcacheX --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
