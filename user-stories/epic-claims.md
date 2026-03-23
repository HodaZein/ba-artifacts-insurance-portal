# Epic - Claims

### US-CL-01 submit FNOL (motor / home)
As a policyholder who suffered a loss I want to report it through the portal so I don't have to wait on the phone.

AC:
- motor or home policy only (travel claims out of scope for MVP)
- on submit, claim is created in claims system + reference number returned to user
- max 10 attachments, max 10MB each (anything over -> reject with clear message)
- if claims system is down: save the draft locally and tell the user to retry. do not lose the data.

### US-CL-02 see current status of my claim
As a policyholder with an open claim I want to see its current status so I know what's happening without calling.

AC:
- "My claims" lists status, last update timestamp, assigned handler name
- when the handler updates the claim, the new status shows up in the portal within 1 min (webhook)

### US-CL-03 message my claim handler
- send + receive messages tied to a specific claim
- handler sees it in the claims system within 1 min
- when handler replies, customer gets an email notification + sees the message on next portal visit

note: messaging is "Should" priority for MVP (see SRS F-11). if we are running short on capacity in sprint 5 this can slip to v1.1.
