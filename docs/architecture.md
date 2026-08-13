# Architecture

Relent is structured as a local-first mobile product with optional authenticated services.

```mermaid
flowchart LR
    UI["Mobile interface"] --> F["Structured check-in flow"]
    F --> D["Deterministic decision logic"]
    D --> R["Result and action selection"]
    R --> H["Local history and learning"]
    H --> E["Encrypted local persistence"]
    E -. "optional" .-> SY["Authenticated synchronization"]
    SY -. "bounded requests" .-> AI["External AI service"]
```

## Main boundaries

- **Interface:** onboarding, check-ins, results, actions, progress, and account controls.
- **Product logic:** structured inputs are converted into versioned product state and deterministic outputs.
- **Persistence:** product history is stored locally, with encryption applied before it reaches the storage layer.
- **Cloud services:** authentication, optional synchronization, notifications, and bounded server operations.
- **External services:** optional AI processing, analytics, and error monitoring, each with separate controls.

The diagram deliberately omits production identifiers, schemas, endpoints, security configuration, prompts, and internal operational tooling.
