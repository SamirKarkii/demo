# TechHive - Smart Gadget Store

## System Flowchart

```mermaid
flowchart TD
    A[Start] --> B[Dashboard]
    B --> C[Login]
    C --> D[Check Credentials]
    D --> E{Valid?}
    E -->|No| F[Error]
    F --> C
    E -->|Yes| G{Admin?}
    G -->|Yes| H[Admin Page]
    H --> I[Manage Products]
    I --> J[Logout]
    J --> K[End]
    G -->|No| L[User Page]
    L --> M[Browse Products]
    M --> N[Add to Cart]
    N --> O{Checkout?}
    O -->|No| L
    O -->|Yes| P[Payment Type]
    P --> Q[Online Payment]
    P --> R[Cash on Delivery]
    Q --> S{Success?}
    S -->|No| P
    S -->|Yes| T[Order Placed]
    R --> T
    T --> J
