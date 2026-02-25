<ast_consistency>
Directive: Code must be instantly recognizable, minimizing parsing time for the human reviewer.
</ast_consistency>

naming_conventions>
- Interfaces/Types: [e.g., PascalCase, no "I" prefix (e.g., `User`, not `IUser`)].
- Constants: [e.g., UPPER_SNAKE_CASE].
- Booleans: MUST be prefixed with `is`, `has`, `can`, or `should`.
</naming_conventions>

<structural_rules>
1. EARLY RETURNS: Use guard clauses to exit functions early. Nested `if/else` statements deeper than 2 levels are forbidden.
2. EXPORTS: Use named exports strictly. Default exports are prohibited to ensure predictable refactoring across the codebase.
3. COMMENTS: Do NOT comment to explain *what* code does (the AST should be self-documenting). ONLY comment to explain *why* a non-obvious technical decision was made.
</structural_rules>
