# Epic — Identity & access

## US-IA-01 · Register with email and password
> **As a** prospective portal user
> **I want** to register with my email and a password
> **so that** I can access the portal without calling the carrier.

**Acceptance criteria**
- **Given** I am on the registration page
  **When** I enter a valid email and a password meeting the policy
  **Then** my account is created and a verification email is sent.
- **Given** I have not verified my email
  **When** I attempt to log in
  **Then** I am told to verify my email and offered to resend the link.
- **Given** I enter an email already registered
  **When** I submit the form
  **Then** I see a generic "if this email is registered, we have sent
  instructions" message (no account enumeration).

**Notes**
- Password policy: ≥ 12 chars, at least one digit, one symbol.
- Verifcation link valid 24 h.

---

## US-IA-02 · Log in with email and password
> **As a** registered user
> **I want** to log in
> **so that** I can use the portal.

**Acceptance criteria**
- **Given** correct credentials
  **When** I submit the login form
  **Then** I am taken to the policy overview.
- **Given** five consecutive failed attempts within 10 minutes
  **When** I attempt again
  **Then** the account is temporarily locked for 15 minutes and I am
  informed.

---

## US-IA-03 · Enable optional MFA
> **As a** security-conscious user
> **I want** to enable a TOTP MFA app
> **so that** my account is protected even if my password leaks.

**Acceptance criteria**
- **Given** I am logged in
  **When** I open "Security" and scan the QR code with an authenticator
  **Then** MFA is enabled after I confirm with one valid code.
- **Given** MFA is enabled
  **When** I log in
  **Then** I am asked for a TOTP code after the password.
- **Given** I lose my MFA device
  **When** I use a recovery code
  **Then** I am logged in and prompted to re-enable MFA.
