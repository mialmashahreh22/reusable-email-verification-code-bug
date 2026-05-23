# Bug Report: Reusable Email Verification Code Bug

## Summary

Requesting a new email verification code does not invalidate older codes, leaving multiple valid codes active at once.

## Vulnerability Type

Token Lifecycle / Verification Logic

## Severity

Medium

## Related CWE

CWE-287: Improper Authentication

## Steps to Reproduce

1. Start email verification.
2. Request a code.
3. Use resend to request another code.
4. Submit the first code.
5. Observe that it still works.

## Expected Behavior

When a new verification code is issued, all previous codes for the same purpose should be invalidated.

## Actual Behavior

Old and new verification codes remain valid simultaneously.

## Impact

- An older leaked or intercepted code remains usable.
- Verification integrity is weakened.
- Attack surface increases around email identity proof.

## Remediation

- Invalidate old verification codes on resend.
- Store expiry and one-time-use status.
- Limit resend frequency and log suspicious attempts.

## Evidence Guidance

For a real responsible disclosure report, include only authorized evidence:

- Redacted screenshots
- Redacted request and response examples
- Timeline of testing
- Clear reproduction steps
- No real secrets, tokens, private personal data, or destructive live actions

## CTF Lab

The lab in `labs/ctf-game` teaches this bug class using safe mock data. Complete all missions to reveal the flag.
