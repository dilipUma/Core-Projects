# CLAUDE.md — Core-Projects

This file provides guidance for AI assistants (and human contributors) working in this repository.

## Repository Overview

**Core-Projects** is a mono-repository for shared core libraries and services. It is currently in its initial setup phase with no application code yet.

## Project Structure

```
Core-Projects/
├── CLAUDE.md          # This file — AI assistant guidance
└── (new modules to be added here)
```

As the repository grows, expect a structure such as:

```
Core-Projects/
├── CLAUDE.md
├── README.md
├── .gitignore
├── packages/          # Shared libraries / modules
├── services/          # Backend services
├── scripts/           # Build and utility scripts
├── docs/              # Documentation
└── tests/             # Integration / end-to-end tests
```

## Development Workflow

### Branch Naming

- Feature branches: `feature/<short-description>`
- Bug fixes: `fix/<short-description>`
- AI-generated branches: `claude/<description>-<session-id>`

### Commit Messages

- Use imperative mood: "Add feature" not "Added feature"
- Keep the subject line under 72 characters
- Reference issue numbers where applicable (e.g., `Fix #42`)

### Pull Requests

- PRs should target the `main` branch unless otherwise specified
- Include a summary of changes and a test plan
- Keep PRs focused — one logical change per PR

## Build & Test

No build system or test framework has been configured yet. Update this section when tooling is added.

```bash
# Placeholder — update when build tooling is set up
# npm install / pip install / cargo build / etc.
# npm test / pytest / cargo test / etc.
```

## Key Conventions

1. **Keep it simple** — prefer straightforward solutions over clever abstractions.
2. **Document decisions** — when making architectural choices, note the reasoning.
3. **No secrets in code** — never commit credentials, API keys, or `.env` files.
4. **Consistent formatting** — adopt and enforce a formatter/linter as soon as code is added.

## For AI Assistants

- **Read before writing.** Always read existing files before proposing changes.
- **Minimal diffs.** Only change what is necessary to accomplish the task.
- **Don't over-engineer.** Avoid adding abstractions, utilities, or features beyond what is requested.
- **Run checks.** Once a build/test system is in place, always run tests and linting before committing.
- **Ask when uncertain.** If requirements are ambiguous, ask for clarification rather than guessing.
- **Update this file.** When new tooling, patterns, or conventions are established, update this CLAUDE.md to reflect them.
