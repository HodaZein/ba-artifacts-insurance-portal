# FNOL — First Notice of Loss

```mermaid
flowchart TD
    A([Customer opens FNOL]) --> B[Select policy]
    B --> C[Enter loss date and time]
    C --> D[Select loss cause from list]
    D --> E[Describe what happened]
    E --> F[Attach photos / documents]
    F --> G{Validations pass?}
    G -- No --> H[Show field errors]
    H --> C
    G -- Yes --> I[Show summary for review]
    I --> J{Customer confirms?}
    J -- No --> C
    J -- Yes --> K[Submit to claims system]
    K --> L{Claims system accepts?}
    L -- No --> M[Show retry / contact us]
    L -- Yes --> N[Show claim reference + ETA]
    N --> O[Email confirmation sent]
    O --> Z([End])
```

**Notes:**
- Maximum 10 attachments, 10 MB each (see SRS F-09).
- Loss-cause list is sourced from the claims system to keep parity.
- On submission failure the draft is saved locally so the customer can
  retry without re-entering data.
