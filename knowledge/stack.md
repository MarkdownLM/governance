<stack_definitions>
Language: [e.g., TypeScript 5.x]
Frameworks: [e.g., React 18 (Server Components only), Fastify 4.x]
</stack_definitions>

<syntax_invariants>
1. TYPE SAFETY: `any` is strictly forbidden. `unknown` is permitted only when followed by a type-narrowing validation guard.
2. MODULES: ESM (`import`/`export`) is strictly required. CommonJS (`require`) is a violation.
3. ASYNC: Use `async/await` strictly. `.then().catch()` chains are forbidden for readability.
4. NULLABILITY: Strict null checks MUST be enabled. Handle `undefined` and `null` explicitly at the IO boundary.
</syntax_invariants>
# Tech Stack Rules

## 1. Approved Frameworks
*   **Frontend:** React / Next.js
*   **Backend:** Node.js / Express (or framework specific to your org)
*   **Database:** PostgreSQL

## 2. Library Restrictions
*   **State Management:** Use robust solutions like Zustand or React Context; avoid unnecessary Redux boilerplate.
*   **Styling:** TailwindCSS is preferred for rapid, consistent UI development.

## 3. Versioning Requirements
*   Always use the latest LTS (Long Term Support) node version.
*   Pin dependencies in `package.json` to avoid unexpected breaking changes during CI/CD.

## 4. Banned Technologies
*   Avoid adding experimental beta frameworks to production data paths.
