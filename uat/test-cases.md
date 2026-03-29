# UAT Test Cases

Selected sample. Full set lives in Jira (`PORTAL` project).

| ID       | Title                                       | Linked story | Priority |
|----------|---------------------------------------------|--------------|----------|
| TC-001   | Register with valid email and strong pwd    | US-IA-01     | High     |
| TC-002   | Register with already-used email            | US-IA-01     | High     |
| TC-003   | Login lockout after 5 failed attempts       | US-IA-02     | High     |
| TC-004   | Enable MFA via authenticator app            | US-IA-03     | Medium   |
| TC-010   | View policy list with > 10 policies         | US-PD-01     | Medium   |
| TC-011   | Download motor policy schedule (PDF)        | US-PD-02     | High     |
| TC-012   | Download certificate of insurance — motor   | US-PD-03     | High     |
| TC-013   | Certificate hidden for non-motor policies   | US-PD-03     | Medium   |
| TC-020   | Update postal address (EU)                  | US-PM-01     | High     |
| TC-021   | Address update outside EU shows manual hint | US-PM-01     | Medium   |
| TC-022   | Email change requires verification          | US-PM-03     | High     |
| TC-030   | Submit motor FNOL with 3 photos             | US-CL-01     | High     |
| TC-031   | FNOL rejects 11th attachment                | US-CL-01     | Medium   |
| TC-032   | FNOL retry when claims system down          | US-CL-01     | High     |
| TC-040   | View open claim status                      | US-CL-02     | High     |
| TC-041   | Status update visible within 1 minute       | US-CL-02     | Medium   |
| TC-050   | Send message to claim handler               | US-CL-03     | Medium   |

## Sample case detail — TC-030
**Pre-conditions:** Customer logged in, holds at least one active motor
policy.

| Step | Action                                              | Expected result                              |
|------|-----------------------------------------------------|----------------------------------------------|
| 1    | Open "Report a claim"                               | List of eligible policies shown              |
| 2    | Select motor policy                                 | FNOL form displayed                          |
| 3    | Enter loss date = yesterday, time = 18:30           | Field accepted                               |
| 4    | Select cause "Collision with another vehicle"       | Field accepted                               |
| 5    | Enter description (≥ 20 chars)                      | Field accepted                               |
| 6    | Attach 3 JPG photos (~2 MB each)                    | Photos listed, removable                     |
| 7    | Click "Review"                                      | Summary screen with all entered data         |
| 8    | Click "Submit"                                      | Success page with claim reference            |
| 9    | Check inbox                                         | Confirmation email received                  |
| 10   | Open "My claims"                                    | New claim listed with status "Submitted"     |
