# Agentic Skills: Software Engineering & Code Quality

> Core engineering excellence skills: anti-slop enforcement, unlazy development gates, test-driven development (TDD), AI regression suites, and architectural decision records.

This repository is part of the **Open Agentic Skills Catalog**. It provides modular, self-contained, and security-hardened skills for autonomous agents (Claude Code, Cursor, Codex, OpenClaw, Gemini CLI, and Antigravity).

## Skills Included (12)

| Skill | Description |
|---|---|
| [`anti-slop`](skills/anti-slop) | Comprehensive toolkit for detecting and eliminating AI slop - generic, low-quality AI-generated patterns in natural language, code, and design. Use when reviewing or improving content quality, preventing generic AI patterns, cleaning up existing content, or enforcing quality standards in writing, code, or design work. |
| [`tdd-workflow`](skills/tdd-workflow) | Use this skill when writing new features, fixing bugs, or refactoring code. Enforces test-driven development with 80%+ coverage including unit, integration, and E2E tests. |
| [`ai-regression-testing`](skills/ai-regression-testing) | Regression testing strategies for AI-assisted development. Sandbox-mode API testing without database dependencies, automated bug-check workflows, and patterns to catch AI blind spots where the same model writes and reviews code. Use when adding regression coverage to AI-assisted code, or when the same model both wrote and reviewed a change. |
| [`architecture-decision-records`](skills/architecture-decision-records) | Capture architectural decisions made during Claude Code sessions as structured ADRs. Auto-detects decision moments, records context, alternatives considered, and rationale. Maintains an ADR log so future developers understand why the codebase is shaped the way it is. |
| [`living-docs-governance`](skills/living-docs-governance) | Keep a long-lived projects documentation from rotting by assigning existing project docs clear constitution, map, status, and history roles, then wiring the active agent harness to those canonical sources. Use in the maintain phase when docs drift from code, agents lose context between sessions, or intentional removals keep being recreated. Prefer adopting the repositorys current docs structure over creating new root files. 中文触发：文档治理、活文档、项目状态追踪、防文档漂移、项目地图、健康仪表盘、删除区、长期项目治理 |
| [`intent-driven-development`](skills/intent-driven-development) | Turn ambiguous or high-impact product and engineering changes into scoped, verifiable acceptance criteria before or alongside implementation. Use when a user asks to clarify a feature, define acceptance criteria, de-risk a security/data/migration/integration change, prepare implementation requirements for another agent, or make a complex request testable. Do not trigger for trivial edits, straightforward fixes, active debugging, code review, or implementation requests whose acceptance conditions are already clear unless the user explicitly invokes this skill. |
| [`error-handling`](skills/error-handling) | Patterns for robust error handling across TypeScript, Python, and Go. Covers typed errors, error boundaries, retries, circuit breakers, and user-facing error messages. Use when designing error types, retries, circuit breakers, or user-facing failure messages in TypeScript, Python, or Go. |
| [`git-workflow`](skills/git-workflow) | Git workflow patterns including branching strategies, commit conventions, merge vs rebase, conflict resolution, and collaborative development best practices for teams of all sizes. Use when choosing a branching strategy, writing commit conventions, deciding merge versus rebase, or resolving conflicts. |
| [`codehealth-mcp`](skills/codehealth-mcp) | Real-time structural Code Health via CodeScene MCP — review before edits, verify score deltas after changes, gate commits and PRs. Use when reviewing code quality, refactoring, checking if AI changes degraded a file, or before commit/PR. |
| [`production-audit`](skills/production-audit) | Local-evidence production readiness audit for shipped apps, pre-launch reviews, post-merge checks, and what breaks in prod? questions without sending repo data to an external audit service. Use when auditing production readiness before launch, after a merge, or when asked what breaks in prod. |
| [`click-path-audit`](skills/click-path-audit) | Trace every user-facing button/touchpoint through its full state change sequence to find bugs where functions individually work but cancel each other out, produce wrong final state, or leave the UI in an inconsistent state. Use when: systematic debugging found no bugs but users report broken buttons, or after any major refactor touching shared state stores. |
| [`ponytail`](skills/ponytail) | > |

## Installation & Usage

### 1. Claude Code
Clone or symlink the desired skill folder directly into your workspace `.claude/skills/` or global `~/.claude/skills/`:

```bash
# Example: install a specific skill into your current workspace
mkdir -p .claude/skills
cp -r skills/anti-slop .claude/skills/
```

### 2. Antigravity & Generic Agent Harnesses
Copy the skill into your `.agents/skills/` directory:

```bash
mkdir -p .agents/skills
cp -r skills/* .agents/skills/
```

### 3. Cursor & Windsurf
Reference the rule or skill inside your `.cursorrules` or `.windsurfrules`.

## Security & Privacy Guarantee

- **Zero Private Credentials**: All keys, webhooks, and secrets are parameterized as environment variables (`process.env.API_KEY`).
- **Zero PII**: Contains no private emails, phone numbers, or proprietary business tokens.
- **Open License**: Released under the [MIT License](LICENSE).
