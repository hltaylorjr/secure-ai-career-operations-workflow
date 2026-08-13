# Architecture and data flow

## Component model

```mermaid
flowchart TB
    subgraph Public["Public surface"]
        W["Professional website"]
        Q["Career-focused AI Q&A"]
        V["AI voice contact"]
    end

    subgraph Boundary["Validated boundary"]
        API["Server-side API controls"]
        WH["Signed event intake"]
        SAN["Sanitization and policy enforcement"]
    end

    subgraph Private["Private career operations"]
        T["Opportunity and interaction tracker"]
        D["Approved document library"]
        C["Scoped career calendar"]
        R["Reminders and review queue"]
    end

    subgraph Human["Human governance"]
        A["Review and approval"]
        E["External action"]
    end

    W --> Q
    W --> V
    Q --> API
    V --> WH
    API --> SAN
    WH --> SAN
    SAN --> T
    D --> A
    T --> A
    C --> A
    R --> A
    A --> E
```

## Trust boundaries

1. **Public surface:** accepts only limited professional inquiries and career-related questions.
2. **Validated boundary:** authenticates events, validates inputs, enforces policy, removes unsafe content, and applies limits.
3. **Private operations:** stores approved records with restricted access and defined purposes.
4. **Human governance:** reviews consequential drafts before submission, communication, scheduling, or disclosure.

## External-content rule

Job postings, messages, résumés, uploaded files, caller claims, links, and portal instructions are untrusted until verified. They cannot override system policy or authorize disclosure or external action.

## Caller-identity rule

Network-presented caller identification is recorded, when available, only as **unverified caller ID**. It may be blocked, unavailable, restricted, or spoofed.

