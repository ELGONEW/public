# CLAUDE.md

Guidance for AI assistants (Claude Code and others) working in this repository.

## Repository status

**This repository is currently empty** — it has no source code, no commits on
the default branch, and no established build system as of 2026-06-17. This file
is a starting scaffold. As code lands, **keep this document current**: replace
the placeholder sections below with the real project structure, commands, and
conventions, and remove this status note once the repo has a meaningful codebase.

- Remote: `elgonew/public` (`origin`)
- Default branch: not yet created (the remote reports an empty repository)

## How to update this file as the project grows

When real code is added, this document should describe at minimum:

1. **What the project is** — its purpose and the problem it solves.
2. **Tech stack & layout** — languages, frameworks, and the top-level directory
   structure (point to the directories that matter, not an exhaustive tree).
3. **Build / run / test commands** — the exact commands to install dependencies,
   build, run locally, and run the test suite and linters. Prefer documenting
   commands you have actually run and verified.
4. **Conventions** — code style, naming, commit/PR conventions, and any
   project-specific patterns an assistant should follow rather than guess.
5. **Gotchas** — non-obvious constraints, required environment variables, or
   setup steps that aren't discoverable from the code alone.

Keep entries concise and high-signal. Document what is non-obvious; don't
restate what the code already makes clear.

## Git workflow

- **Branching:** Do development on dedicated feature branches. The current
  working branch is `claude/claude-md-docs-58gd6r`. Never push to another
  branch without explicit permission.
- **Commits:** Write clear, descriptive commit messages.
- **Push:** Use `git push -u origin <branch-name>`. On network failures, retry
  with exponential backoff.
- **Pull requests:** Do not open a PR unless explicitly asked.

## Notes for assistants

- This repo had no existing `CLAUDE.md`; this is the first one.
- Because there is no code yet, do not invent project structure, commands, or
  conventions. When the codebase exists, analyze it directly and rewrite the
  placeholder sections above with verified, specific details.
