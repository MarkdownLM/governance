<fault_tolerance_protocol>
Directive: Fail fast, log predictably, degrade gracefully.
</fault_tolerance_protocol>

<error_pipeline>
1. CATCH BOUNDARIES: Async execution boundaries MUST be wrapped in generic handlers to prevent unhandled promise rejections crashing the process.
2. STRUCTURED TELEMETRY: All logged errors MUST output strictly as JSON, containing `traceId`, `userId`, `errorCode`, and `context`.
3. EXPOSURE: Internal system errors (stack traces, DB syntax) MUST NEVER cross the network boundary to the client. Map to standard RFC 7807 Problem Details.
</error_pipeline>

<panic_rules>
 - Use explicit `Result<T, E>` types or custom Error subclasses (e.g., `DomainError`, `InfrastructureError`). DO NOT throw primitive strings or generic `Error` objects.
</panic_rules>
