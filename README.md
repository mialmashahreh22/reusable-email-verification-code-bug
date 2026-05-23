# Reusable Email Verification Code Bug

<p align="center">
  <img src="https://img.shields.io/badge/Bug_Report-Cybersecurity-0078D4?style=for-the-badge" alt="Bug Report">
  <img src="https://img.shields.io/badge/CTF_Lab-Playable-22C55E?style=for-the-badge" alt="CTF Lab">
  <img src="https://img.shields.io/badge/Category-Token_Lifecycle_%2F_Verification_Logic-F97316?style=for-the-badge" alt="Token Lifecycle / Verification Logic">
  <img src="https://img.shields.io/badge/Severity-Medium-DC2626?style=for-the-badge" alt="Medium">
</p>

---

## Overview

Requesting a new email verification code does not invalidate older codes, leaving multiple valid codes active at once.

This repository is a **sanitized educational case study**. It does not target a real company or live system. The included lab uses mock data so students can safely understand the bug class.

## Quick Facts

| Field | Value |
|---|---|
| Category | Token Lifecycle / Verification Logic |
| Severity | Medium |
| Related CWE | CWE-287: Improper Authentication |
| Lab | Browser-based CTF |
| Flag Style | `FLAG{...}` |

## Play the CTF Lab

Run locally:

```bash
python -m http.server 8000
```

Open:

```text
http://localhost:8000/labs/ctf-game/
```

Goal: solve the three missions and reveal the flag.

## Report

Read the full report:

```text
report/BUG-REPORT.md
```

## Impact Summary

- An older leaked or intercepted code remains usable.
- Verification integrity is weakened.
- Attack surface increases around email identity proof.

## Repository Structure

```text
reusable-email-verification-code-bug/
|-- README.md
|-- report/
|   `-- BUG-REPORT.md
|-- docs/
|   `-- remediation.md
|-- labs/
|   `-- ctf-game/
|       |-- index.html
|       |-- styles.css
|       |-- app.js
|       |-- manifest.webmanifest
|       |-- service-worker.js
|       `-- assets/
|           `-- ctf-icon.svg
`-- resources/
    `-- references.md
```

## Safety

Use this project only for learning, local labs, and responsible disclosure practice. Do not test destructive actions, IDORs, token exposure, or business-logic abuse against systems you do not own or have permission to test.
