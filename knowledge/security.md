<security_posture>
Directive: Zero-Trust Architecture. Assume all input is hostile.
</security_posture>

<hard_security_rules>
1. AUTHORIZATION: Every single endpoint/controller MUST explicitly assert the principal's RBAC/ABAC permissions before executing logic. Default to DENY.
2. INJECTION PREVENTION: ORM/Query builders MUST be used strictly. String interpolation in database queries is a FATAL execution violation.
3. SANITIZATION: Data crossing the client boundary MUST be sanitized for XSS. 
4. CRYPTOGRAPHY: When handling sensitive PII or tokens, use constant-time comparison functions to prevent timing attacks.
</hard_security_rules>

<anti_patterns>
- Logging sensitive PII, Bearer tokens, or passwords.
- Trusting JWT payloads without verifying the cryptographic signature.
</anti_patterns>
