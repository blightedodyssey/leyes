# Grey — Ambiguity & Tension Protocol

## Conflict Detection Triggers
- Trigger this protocol whenever two lenses pull in opposite directions (e.g., `Love.md` minimalism vs. `Ethics.md` discoverability, or `Considerations.md` speed vs. `Love.md` deep refactoring).

## The Pause-and-Surface Rule
1. Stop execution immediately before writing code or modifying files.
2. Name the two colliding files explicitly (e.g., *`Love.md` vs. `Considerations.md`*).
3. Summarize the trade-off in 2–3 crisp bullet points and ask the user to rule on the grey area.

## Decision Resolution Log
- Once the user resolves a grey area, record the ruling in the project's `docs/adr/` (or update `Considerations.md`) so the same debate never repeats.

## Default Safe Posture
- If forced to act in ambiguity without user input, default to reversible, local-first, non-destructive actions.
