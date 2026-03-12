# To-be: Service request via portal

```mermaid
flowchart TD
    A([Customer needs a service]) --> B[Customer opens portal]
    B --> C{Logged in?}
    C -- No --> D[Login or register]
    D --> E{MFA enabled?}
    E -- Yes --> F[MFA challenge]
    E -- No --> G[Authenticated session]
    F --> G
    C -- Yes --> G
    G --> H{Selects task}
    H -->|Download document| I[Portal fetches from policy admin]
    H -->|Update address| J[Portal updates + writes audit log]
    H -->|FNOL| K[FNOL flow - see fnol.md]
    H -->|Claim status| L[Portal queries claims system]
    I --> Z([Done])
    J --> Z
    K --> Z
    L --> Z
```

**Expected effects:**
- Identity verified once at login (with optional MFA).
- Documents available in seconds, not minutes.
- Audit trail captured automatically for every change.
