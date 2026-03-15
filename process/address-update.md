# Address update

```mermaid
flowchart TD
    A([Customer opens "My data"]) --> B[Edit address]
    B --> C{Country in EU?}
    C -- No --> D[Show "contact us" - manual review]
    C -- Yes --> E[Validate postal format]
    E --> F{Valid?}
    F -- No --> G[Show inline error]
    G --> B
    F -- Yes --> H[Show diff: old vs new]
    H --> I{Customer confirms?}
    I -- No --> B
    I -- Yes --> J[Persist + write audit entry]
    J --> K[Show success]
    K --> Z([End])
```
