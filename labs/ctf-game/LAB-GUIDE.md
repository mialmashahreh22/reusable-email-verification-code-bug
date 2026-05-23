# Reusable Email Verification Code Bug - CTF Lab Guide

This lab is a realistic mock simulation for one bug class.

## Goal

Find the bug in the mock app and unlock the flag.

## How to Run

From this repo root:

```bash
python -m http.server 8000
```

Open:

```text
http://localhost:8000/labs/ctf-game/
```

## What to Do

1. Request the first verification code.
2. Resend to generate a second code.
3. Submit the old first code.
4. The old code still verifies and unlocks the flag.

## What You Should Learn

Security tokens should have clear lifecycle rules: one-time use, expiry, and invalidation on replacement.

## Safety

This is a local mock app. Do not repeat these actions against real websites unless you have explicit authorization.
