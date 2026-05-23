# Reusable Email Verification Code Bug - Bug Explanation

## What Is the Bug?

Requesting a new email verification code does not invalidate the old one, so multiple codes remain valid.

## Vulnerability Type

Token Lifecycle / Verification Logic

## Why It Happens

The system stores issued codes but does not mark older codes as expired when a replacement code is generated.

## Why It Matters

Security tokens should have clear lifecycle rules: one-time use, expiry, and invalidation on replacement.

## Safe Lab Version

This repository includes a safe local simulation of the bug. The lab does not contact any real target or live service.

Lab path:

```text
labs/ctf-game/
```

## How to Fix

- Invalidate old verification codes when a new one is issued.
- Store token purpose, expiry, and used status.
- Rate-limit resend attempts and log suspicious token activity.

## Responsible Disclosure Note

For a real report, keep evidence redacted, avoid publishing secrets or private user data, and test only systems where you have permission.
