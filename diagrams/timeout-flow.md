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
