# Epic - identity & access

### US-IA-01 register with email + password
As a prospective portal user I want to register with my email and a password so that I can access the portal without calling the carrier.

AC:
- valid email + password meeting policy -> account created, verification email sent
- if email not verified yet and user tries to log in -> tell them to verify, offer resend
- if email is already registered -> show the generic "if this email is registered, we have sent instructions" (no account enumeration)

notes:
- password policy: >= 12 chars, at least one digit, one symbol
- verification link valid 24h

### US-IA-02 log in with email + password
As a registered user I want to log in so I can use the portal.

AC:
- correct credentials -> taken to policy overview
- 5 failed attempts in 10 minutes -> account locked 15 min, user is told

### US-IA-03 enable optional MFA
As a security-conscious user I want to enable a TOTP MFA app so my account is protected even if my password leaks.

AC:
- "Security" page -> scan QR with authenticator -> confirm one valid code -> MFA enabled
- with MFA enabled, login asks for the TOTP code after the password
- if I lose my MFA device, recovery code logs me in and prompts me to re-enable MFA
