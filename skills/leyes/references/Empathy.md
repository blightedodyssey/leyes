# Empathy — User & Maintainer Reality

## Hardware & Network Reality
- Respect finite RAM/VRAM, multi-machine workflows, offline resilience, and varying bandwidth.
- **RAM Headroom Rule:** Keep total local model + agent + IDE memory under 75% of physical RAM (leaving at least 25% headroom for OS + swap, e.g., ~12GB max on a 16GB machine).
  - Verify available memory with `free -h` (Linux) or equivalent before spawning heavy local models
  - Heavy reasoning, planning, and coding go to configured cloud endpoints when local headroom is tight
- Design local setups to degrade gracefully when cloud APIs or external services are unreachable.
- **Offline Resilience Verification:** For any tool or workflow claiming offline capability, add an explicit offline smoke test (network disabled) to CI—verify the claim, don't just document it.

## Maintenance & Cognitive Load
- Every added dependency, abstraction, or file carries future upkeep cost—keep architectures lean.
- **Tiered Dependency Audit:**
  - **Lightweight utilities:** Quick 5-second sanity check (last release within 2 years, reasonable issue count)
  - **Heavyweight dependencies** (frameworks, ORMs, bundlers): Full checklist before adding:
    - Last commit date & maintenance status
    - Open critical issues & bus factor
    - License compatibility
    - Viable alternatives comparison
- Optimize for long-term readability over short-term cleverness.

## Environment & Cost Discipline
- **Cross-OS Compatibility Scope:** Default to Linux-first execution; enforce and test Windows/macOS compatibility only when:
  - Multi-OS support is an explicit requirement, OR
  - Code touches system-dependent APIs (paths, shells, permissions, line endings)
- Maximize local/free compute and lean context budgets before reaching for paid resources.

## UX / Resilience
- Favor plain, actionable error messages over raw stack traces so users are never stranded.