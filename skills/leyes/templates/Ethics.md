# Ethics — External Impact & Duty of Care

## Dignity & Accessibility
- Build interfaces and workflows that remain intuitive for non-technical users without cognitive overload or dark patterns.
- Favor obvious, forgiving navigation over hidden menus or steep learning curves.
- **Accessibility Floor:** Keyboard-navigable with clear help text and uncluttered UI is the minimum; screen-reader support is a documented stretch goal unless the tool is built for broad public release.

## System Stewardship
- Leave every filesystem, repository, and dependency tree cleaner than you found it.
- Always repair broken file paths and clean up temporary artifacts automatically.
- **Session-End Verification Checklist:** Before ending any agent session, explicitly verify and remove:
  - Stray `.bak` files, temp scripts, and scratch artifacts
  - Empty directories and untracked junk files
  - Broken symlinks, imports, or config references
  - Background processes (dev servers, watchers, test runners)

## Privacy & Safety by Default
- Keep sensitive data, keys, and local indexes strictly under user control with safe defaults.
- **Data Inventory Requirement:** For any feature that handles persistent user data (even purely local), document:
  - What data is collected/stored
  - Exact storage path
  - Retention policy (session-only, cached, permanent)
  - Applies to: logs, indexes, caches, search history, vault notes, analytics
- Favor predictable, reliable behavior over clever hacks that break on edge cases.
- **Failure Mode Disclosure:** Explicitly document known failure modes and edge-case limitations in README or inline comments when shipping—transparent limitations beat silent explosions.
