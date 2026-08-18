# dev-guidelines-skill

Agent Skill for OrangeChat (also compatible with Claude Code / any Agent Skills runtime).

Import this repo URL into OrangeChat **Agent Skills**, or point any SKILL.md-compatible runtime at `SKILL.md`.

## What it enforces

1. **One-pass delivery** — all requirements complete in a single pass, synchronized fixes across the codebase, no partial patches.
2. **No assumptions** — ambiguity → stop and ask immediately.
3. **Honest limitations** — infeasible requirements get refused directly; alternatives only through a strict three-step protocol, user decides.
4. **Search-first verification** — official docs beat guesses, every time.
5. **Clean delivery** — full files only, no bloat.
6. **Real error handling** — no empty catch blocks, no raw stdout prints, structured logging with location + stack trace + context.
