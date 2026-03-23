# Epic - Personal data

### US-PM-01 update postal address
As a policyholder who moved I want to update my postal address so that my correspondence reaches me.

AC:
- valid EU address: confirm on diff screen, save, write audit entry
- non-EU address: tell the user it needs manual review, give a contact link, do not save anything

### US-PM-02 update phone number
As a policyholder I want to update my phone number so the carrier can reach me.

AC:
- accepted format: E.164 (e.g. +43 660 1234567)
- on save: persist + audit entry

### US-PM-03 update email (with re-verification)
This one is tricky because email is also the login. We do NOT change the login email until the new address is verified.

AC:
- user submits new email -> verification email sent to NEW address
- old address gets a security notification "we received a request to change your email"
- if not verified within 24h the change is silently dropped, login email stays as it was
- once verified -> login email switches, audit entry written

open question: should we require password re-entry before allowing the email change? leaning yes for v2.
