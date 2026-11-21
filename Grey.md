# Grey — Ambiguity & Tension Protocol

## Scope & Precedence (No False Grey)
- **Hard Gates Override Everything:** `Morals.md` (non-negotiables) and `Hate.md` (hard nevers) are never negotiable and never enter `Grey.md`.
- **True Grey Only:** Trigger this protocol only when two active lenses collide (`Love.md` vs. `Ethics.md`, `Love.md` vs. `Considerations.md`, `Ethics.md` vs. `Considerations.md`) or when a requirement is genuinely under-specified.

## Materiality Threshold (Anti-Paralysis Rule)
- **Pause Only on Structural Decisions:** Stop and surface grey areas only when the choice affects public APIs, user-facing UX, data persistence, security, or dependency boundaries.
- **Auto-Resolve Trivial Details:** For purely internal naming, local formatting, or minor helper structure, pick the simplest reversible option and keep moving.

## The Pause-and-Surface Format
When a material grey area is detected, stop before modifying files and output strictly this structure:
- **Collision:** `[Lens A]` vs. `[Lens B]` (1-sentence summary of the clash)
- **Option A (`[Lens A]`-favored):** Concise trade-off and consequence
- **Option B (`[Lens B]`-favored):** Concise trade-off and consequence
- **Question for Superintendent:** Direct question asking which direction to lock in (and why)

## Decision Resolution Log
- Record every settled ruling in the project's `docs/adr/` (or `Considerations.md` if global) using the format: `Date | Collision | Ruling | Rationale`, so the same debate never repeats.

## Default Safe Posture
- If forced to proceed without user input, choose the path that is **local-first, easily reversible, and smallest in blast radius**.
