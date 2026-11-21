# Hate — Anti-Patterns & Hard "Nevers"

## Architectural Smells
- Shallow micro-file fragmentation, bloated "God files," and leaky abstractions.
- **God File Refactor Trigger:** Single files over 500 lines of logic (excluding tests, generated code, pure data/config) warrant a refactor review for separation-of-concerns violations.
- Circular dependencies or hidden cross-module state mutations.

## Workflow Friction
- Unnecessary wrapper tools, heavy background bloatware, and multi-step setup hoops.
- **Anti-Wrapper Rule:** Reject thin wrappers that add <10% value over direct CLI usage—if it's just "alias with a config file," teach the underlying command instead.
- Leaving stray files in `/tmp/` or cluttering project root directories.
- **Immediate Cleanup Discipline:** Remove all `/tmp/` and scratch artifacts before ending a session unless:
  - Explicitly moved to project docs or persistent storage, OR
  - Marked with a `.keep` file explaining why it must persist

## Lazy AI Habits
- Guessing requirements instead of grilling first, or dumping walls of unrequested boilerplate.
- Repeating already-rejected patterns instead of checking ADRs and rules.
- **Shipped Slop (Auto-Reject):**
  - Placeholder `TODO` comments in shipped/production code
  - Example or dummy data left in production configs
  - Copy-pasted license headers without proper attribution
  - Untracked temp files, debug logs, or `.bak` files in git working trees

## UI Clutter
- Noisy dashboards, buried settings, forced account logins, and redundant titles or greetings.
