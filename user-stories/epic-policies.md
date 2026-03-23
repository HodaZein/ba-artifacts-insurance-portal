# Epic - Policies & documents

### US-PD-01 view my policies
As a logged-in policyholder I want to see all my active and historical policies in one place so that I have a single source of truth.

AC:
- when I land on the policy overview I see policy number, product, status, start/end date, premium
- if I have more than 10 policies the list paginates in groups of 10 and there is a search box

### US-PD-02 download policy schedule as PDF
As a policyholder I want to download my policy schedule so that I can prove cover when needed.

AC:
- given I view an active policy, when I click "Download schedule (PDF)" then the PDF downloads within 30s (NFR N-01)
- if the policy admin API is unreachable show a friendly error + "try again later"

### US-PD-03 download certificate of insurance
For motor policies only. As a policyholder of a motor policy I want to download a certificate of insurance so that I can present it to an authority.

AC:
- on a motor policy page a "Certificate of insurance" download is available
- on non-motor policies the certificate option is hidden (don't even show it, no greyed-out)

notes: certificate template is provided by underwriting, do not modify wording.
