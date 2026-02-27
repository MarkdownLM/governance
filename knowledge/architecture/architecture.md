<architecture_topology>
Pattern: [e.g., Modular Monolith / Event-Driven Microservices]
State: [e.g., Stateless API layer, all state deferred to Redis/Postgres]
</architecture_topology>

<boundary_constraints>
1. DOMAIN ISOLATION: Cross-domain communication MUST strictly occur via [e.g., the Event Bus / explicitly defined Service Interfaces].
2. DATA ACCESS: Controller/Transport layers MUST NOT access the database directly. All IO operations MUST be routed through the [e.g., Repository Layer].
3. COUPLING: Hard dependency injection is REQUIRED. Classes/Functions MUST NOT instantiate their own heavy dependencies.
</boundary_constraints>

<forbidden_architecture>
- Circular dependencies between bounded contexts.
- Leaking domain primitives into the HTTP transport layer (e.g., returning raw DB models to the client).
</forbidden_architecture>
