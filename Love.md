# Love — Aesthetic, Ergonomics & Craft

## Architectural Craft
- Deep modules with small, obvious public interfaces, clear separation of concerns, and composable parts.
- **Deep Module Heuristic (Qualitative):** Favor compact public APIs encapsulating substantial internal logic over shallow pass-through wrappers.
  - **Deep (good):** 5-function API managing 500 lines of internal state/logic
  - **Too shallow (bad):** 50-line wrapper around a 10-line function with no added value
- Explicit one-way dependencies and pure, isolated unit tests.

## Visual & UX Taste
- Intentional minimalism, clean typography, uncluttered layouts, and cohesive palettes.
- Cohesive, high-craft polish without visual noise.
- **Design System Requirement:** For any multi-screen or public-facing UI, document a minimal design token spec:
  - Color palette (3–5 semantic colors: primary, background, text, success, error)
  - Font stack (1–2 typefaces with fallbacks)
  - Spacing scale (4–6 values: xs, sm, md, lg, xl)
  - Single-screen internal tools may skip this.

## Learning-First Code
- Self-explanatory structure, domain-aligned naming (`GLOSSARY.md`), and clear separation that teaches as you read.
- **Teaching Through Comments & Commits:**
  - Inline *why* comments for non-obvious decisions: algorithm choices, non-standard API usage, tricky edge-case handling
  - Full commit-body explanations for major architectural shifts or design decision rationale
  - **Socratic Self-Explanation Checkpoints:** When introducing core architectural concepts or language mechanics, explain interactively (not just document) so the user builds real understanding, not just copied patterns.

## Tooling Philosophy
- Fast, keyboard-driven, transparent CLI/TUI workflows with direct control and zero middlemen.
- **Performance Floor for Responsiveness:**
  - CLI/TUI startup: <100ms
  - Interactive command response: <500ms perceived latency
  - Longer operations: explicit progress indicators (spinner, percentage, ETA)
