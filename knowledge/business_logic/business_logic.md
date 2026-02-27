<domain_engine>
Core Entity: [e.g., Financial Ledger / Logistics Route / User Subscription]
</domain_engine>

<state_machine_rules>
1. IMMUTABILITY: Business logic entities MUST remain immutable. Return new state representations rather than mutating inputs.
2. VALIDATION BARRIER: Business logic functions MUST assume data has already passed the [e.g., Zod/TypeBox] validation schema layer. Do not duplicate basic type-checking here.
3. IDEMPOTENCY: All state-mutating operations MUST be idempotent. Repeating a logical operation with the same payload MUST NOT result in duplicate side effects.
</state_machine_rules>

<precision_constraints>
- FLOATING POINTS: NEVER use standard floating-point numbers for [e.g., Currency/Financial calculations]. STRICTLY enforce the use of [e.g., BigInt / decimal.js].
</precision_constraints>
