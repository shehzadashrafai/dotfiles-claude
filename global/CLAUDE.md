# Global Preferences

## Communication
- Be concise. No preamble, no padding, no "Great question!".
- If a task is ambiguous or risky, ask before proceeding — don't guess.
- Flag problems directly. Don't bury concerns at the end.
- No sycophancy.
- If I correct a mistake, suggest a CLAUDE.md update to prevent it recurring.

## Planning
- Large or multi-file tasks: produce a clear plan and wait for approval before writing code.
- Small or obvious tasks: just do it.
- When in doubt about scope, treat it as large.
- Transform imperative instructions into verifiable goals where possible.
  e.g. "Fix the bug" → "Write a failing test that reproduces it, then make it pass."

## Code — General
- Clarity over cleverness.
- Small focused changes over large rewrites.
- Run existing tests before and after any change.
- Never leave debug code, commented-out blocks, or unexplained TODOs.
- Don't modify files outside the scope of the task without asking.
- Don't auto-format unrelated files.
- Don't assume. Surface confusion, tradeoffs, and inconsistencies — don't silently pick an interpretation.
- Don't overcomplicate. If 100 lines solves it, don't write 1000.
- Commit frequently with meaningful messages. One logical change per commit.

## Environment
- WSL2 Ubuntu. All projects live in ~/projects/ — never /mnt/c/.
- Python: always activate venv before running any commands (`source venv/bin/activate`).
- Set up the full dev environment automatically (pip installs, etc.) — don't wait to be asked.

## Tools Available
- Context7 MCP — use for up-to-date library/framework docs. Add "use context7" to relevant prompts.
- Sequential Thinking MCP — use for complex multi-file decisions or architectural choices.
