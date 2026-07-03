# 🔄 Distributed Transactions

```mermaid
flowchart TD

    DT[Distributed Transactions]

    DT --> ACP[Atomic Commit Protocols]
    DT --> CB[Compensation Based]
    DT --> RP[Reliability Patterns]

    ACP --> TPC[2PC]
    ACP --> THPC[3PC]

    CB --> SAGA[Saga]
    CB --> TCC[TCC]

    SAGA --> CH[Choreography]
    SAGA --> OR[Orchestration]

    RP --> OUTBOX[Outbox Pattern]
    RP --> ES[Event Sourcing]
    RP --> COMP[Compensation Transactions]
