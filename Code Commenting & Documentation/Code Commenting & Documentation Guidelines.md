# Code Commenting & Documentation Guidelines

Use comments and documentation to preserve context that cannot be made clear
through names and structure alone.

## When to comment

- Explain why a non-obvious decision, business rule, workaround, or constraint
  exists.
- Document complex algorithms, important edge cases, and concurrency or
  security safeguards.
- Explain platform or dependency workarounds and link to the relevant issue or
  documentation when available.
- Document public APIs and shared modules using the language's conventional
  format when callers need usage, parameter, or return-value details.

## When not to comment

- Do not restate what clear code already says.
- Do not use comments to excuse confusing code; improve names or structure
  first.
- Avoid comments on every line and remove temporary debug notes before
  delivery.

## Maintenance

- Keep comments accurate when behavior changes; delete obsolete explanations.
- Be concise and follow the language or framework's conventional format.
- Use `TODO` or `FIXME` only for specific, actionable follow-up work. Include
  enough context to understand what remains; do not remove valid tracked work
  merely to make a change appear complete.

## Example

```js
// Keep the last selection while refreshing so a temporary network failure
// does not discard the user's in-progress choice.
const selectionToDisplay = refreshedSelection ?? previousSelection;
```

The comment explains the user-facing reason for the fallback rather than
repeating the code.

## Review checklist

- Can clearer code remove the need for this comment?
- Does the comment explain intent or a constraint rather than narrate steps?
- Are public APIs documented where their usage is not self-evident?
- Are comments current, and has temporary debug output been removed?
