<dependency_governance>
Policy: Zero-Cost Abstraction & Minimal Surface Area
</dependency_governance>

<approved_registry>
- State: [e.g., Zustand]
- Validation: [e.g., Zod]
- IO/Network: [e.g., native fetch API ONLY]
</approved_registry>

<strict_limitations>
1. NATIVE FIRST: If the standard library (or native Web API) can achieve the result in under 50 lines of code, DO NOT introduce a third-party dependency.
2. BUNDLE BUDGET: Any UI component or utility function MUST NOT exceed [e.g., 50kb] gzipped. 
3. PROHIBITED: [e.g., moment.js, lodash (use native ES6 methods), heavy monolithic component libraries].
</strict_limitations>
