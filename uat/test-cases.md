# UAT test cases

selected sample.

- TC-001 register with valid email + strong pwd (US-IA-01, high)
- TC-002 register with already-used email - generic msg, no enumeration (US-IA-01, high)
- TC-003 login lockout after 5 failed attempts (US-IA-02, high)
- TC-004 enable MFA via authenticator app (US-IA-03, medium)
- TC-010 view policy list with > 10 policies (US-PD-01, medium)
- TC-011 download motor policy schedule PDF (US-PD-02, high)
- TC-012 download certificate of insurance - motor (US-PD-03, high)
- TC-013 certificate hidden for non-motor policies (US-PD-03, medium)
- TC-020 update postal address EU (US-PM-01, high)
- TC-021 address update outside EU shows manual hint (US-PM-01, medium)
- TC-022 email change requires verification (US-PM-03, high)
- TC-030 submit motor FNOL with 3 photos (US-CL-01, high)
- TC-031 FNOL rejects 11th attachment (US-CL-01, medium)
- TC-032 FNOL retry when claims system down (US-CL-01, high)
- TC-040 view open claim status (US-CL-02, high)
- TC-041 status update visible within 1 minute (US-CL-02, medium)
- TC-050 send message to claim handler (US-CL-03, medium)

## sample case detail - TC-030
preconditions: customer logged in, holds at least one active motor policy.

steps:
1. open "Report a claim" -> list of eligible policies shown
2. select motor policy -> FNOL form displayed
3. enter loss date = yesterday, time = 18:30 -> field accepted
4. select cause "Collision with another vehicle" -> field accepted
5. enter description (>=20 chars) -> field accepted
6. attach 3 jpg photos (~2MB each) -> photos listed, removable
7. click "Review" -> summary screen with all entered data
8. click "Submit" -> success page with claim reference
9. check inbox -> confirmation email received
10. open "My claims" -> new claim listed with status "Submitted"
