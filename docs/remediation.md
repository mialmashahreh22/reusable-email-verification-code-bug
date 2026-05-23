# Remediation Notes

## Main Fixes

- Invalidate old verification codes on resend.
- Store expiry and one-time-use status.
- Limit resend frequency and log suspicious attempts.

## Engineering Checklist

- Add server-side authorization checks.
- Add regression tests for the reported scenario.
- Log suspicious repeated attempts.
- Return minimal response data.
- Document intended business rules.
- Review related endpoints for the same pattern.

## Verification

After remediation, confirm:

- The old step no longer reproduces: Start email verification.
- The old step no longer reproduces: Request a code.
- The old step no longer reproduces: Use resend to request another code.
- The old step no longer reproduces: Submit the first code.
- The old step no longer reproduces: Observe that it still works.
