# 🦉 OZone

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OReconnaissance-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.1-cyan?style=flat-square"/>
</p>

> **OZone** — DNS Enumeration & Zone Inspector ║

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview


OZone is an offline, read-only DNS zone-file auditor that parses BIND-style zone files to detect misconfigurations and security weaknesses. It checks SOA and NS consistency, dangling and wildcard records, SPF/DKIM/DMARC email-authentication posture, and potential subdomain-takeover targets. Findings are mapped to CWE and MITRE ATT&CK, scored and graded, and exported as TXT, Markdown, JSON, CSV or SARIF.

---

## ✨ Features


- BIND-style zone-file parser with $ORIGIN/$TTL directive and record-type awareness
- SOA/NS consistency checks (serial, refresh/retry/expire, lame delegation hints)
- Dangling/wildcard record detection and subdomain-takeover candidate flagging
- Email-authentication posture: SPF, DKIM and DMARC record presence and strength
- CAA, TXT hygiene and TTL-anomaly review
- CWE+ATT&CK mapping, score/grade and TXT/MD/JSON/CSV/SARIF export with --fail-on gating

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage


```bash
./OZone --scan -f sarif -o zone.sarif
./OZone --zone /etc/bind/db.example.com --origin example.com
./OZone -r /mnt/image --fail-on high --json
./OZone --demo
./OZone --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
