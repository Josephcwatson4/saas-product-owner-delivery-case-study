# Timeout Flow

```mermaid
flowchart TD
    A[User opens mobile app] --> B{Is user authenticated?}
    B -- No --> C[Redirect to login]
    B -- Yes --> D[Start inactivity timer]
    D --> E{User active?}
    E -- Yes --> D
    E -- No --> F[Show timeout warning]
    F --> G{User continues session?}
    G -- Yes --> D
    G -- No --> H[Session expires]
    H --> C

## `diagrams/sso-flow.md`

```markdown
# SSO Flow

```mermaid
flowchart TD
    A[Client submits SSO intake] --> B[Validate metadata]
    B --> C{Metadata complete?}
    C -- No --> D[Request missing information]
    D --> A
    C -- Yes --> E[Configure SSO]
    E --> F[Internal testing]
    F --> G{Authentication successful?}
    G -- No --> H[Troubleshoot mapping/certificate issue]
    H --> E
    G -- Yes --> I[Client validation]
    I --> J[Go-live approval]
