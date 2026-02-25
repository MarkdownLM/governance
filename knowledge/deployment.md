<execution_environment>
Target: [e.g., AWS Lambda / Vercel Edge Runtime / Kubernetes Pods]
Runtime: [e.g., Node.js 20.x (Strictly ES Modules) / Rust 1.75]
</execution_environment>

<infrastructure_constraints>
1. COLD STARTS: Code MUST be optimized for cold starts. Avoid heavy global initializations outside the execution handler unless strictly necessary for connection pooling.
2. MEMORY LIMITS: Streaming APIs MUST be used for payloads exceeding [e.g., 5MB] to prevent out-of-memory (OOM) kills.
3. GRACEFUL DEGRADATION: If [e.g., Redis cache] is unreachable, the system MUST fallback to [e.g., Postgres] without crashing the main thread.
</infrastructure_constraints>

<environment_variables>
- ALL environment variables MUST be validated against a schema at compilation/startup. 
- NEVER provide fallback default values for production secrets.
</environment_variables>
