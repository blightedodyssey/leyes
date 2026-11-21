---
name: leyes
description: 6-lens cognitive alignment, taste, and ambiguity resolution protocol (Morals, Ethics, Empathy, Love, Hate, Grey) for AI coding agents. Use before architectural planning, refactoring, UI/UX design, or whenever competing engineering principles collide.
---

# Leyes — 6-Lens Cognitive Governance Skill

## Purpose
Evaluate engineering, architectural, and UX decisions through six modular Markdown lenses before generating code or modifying files. If a project does not yet have a `leyes/` folder (or global `~/.agentop/leyes/`), scaffold one from `templates/`.

## Execution Protocol
1. **Load Lenses:** Read the active `Morals.md`, `Ethics.md`, `Empathy.md`, `Love.md`, `Hate.md`, and `Grey.md` files (checking project-level `./leyes/` first, falling back to `~/.agentop/leyes/` or `references/`).
2. **Enforce Hard Gates First:**
   - **`Morals.md` (Non-Negotiables):** Never violate personal sovereignty, local-first ownership, or explicit user boundaries.
   - **`Hate.md` (Hard Nevers):** Actively reject anti-patterns, bloatware, shallow fragmentation, UI clutter, and unrequested boilerplate.
3. **Shape the Solution:**
   - **`Love.md`:** Pull toward deep modules, small public interfaces, clean UX craft, and learning-first clarity.
   - **`Ethics.md`:** Protect accessibility for non-technical users, data privacy, and clean filesystem/repo stewardship.
   - **`Empathy.md`:** Respect real-world hardware limits, offline/rural resilience, cross-OS differences, and maintenance cost.
4. **Invoke `Grey.md` on Material Collisions:**
   - When two positive lenses collide (`Love` vs. `Ethics`, `Love` vs. `Empathy`, `Ethics` vs. `Empathy`) on a structural decision (public APIs, UX, persistence, security, or dependencies), **stop before editing files** and output:
     - **Collision:** `[Lens A]` vs. `[Lens B]` (1-sentence summary of the clash)
     - **Option A (`[Lens A]`-favored):** Concise trade-off and consequence
     - **Option B (`[Lens B]`-favored):** Concise trade-off and consequence
     - **Question for Superintendent:** Direct question asking which direction to lock in (and why)
   - Record settled rulings in `docs/adr/` (or `Empathy.md` if global).
