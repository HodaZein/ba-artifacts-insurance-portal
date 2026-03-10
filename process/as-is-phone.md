# As-is: Service request via phone

```mermaid
flowchart TD
    A([Customer needs a service]) --> B[Customer calls call centre]
    B --> C{IVR routing}
    C -->|Policy info| D[Agent verifies identity]
    C -->|Claim| D
    C -->|Other| D
    D --> E{Identity OK?}
    E -- No --> F[Agent asks for additional details]
    F --> E
    E -- Yes --> G[Agent looks up policy in core system]
    G --> H{Request type}
    H -->|Document| I[Agent emails PDF from system]
    H -->|Address change| J[Agent updates record + reads back]
    H -->|FNOL| K[Agent collects loss details into ticket]
    I --> Z([End])
    J --> Z
    K --> Z
```

**Pain points observed:**
- Identity verification consumes ~50% of average call time.
- Agents copy policy data manually between systems.
- Document delivery by email is delayed by mail-server queues.
