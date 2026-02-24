# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A collection of reusable boilerplates and templates for Docker Compose, Ansible, Terraform, shell scripts, serverless functions, and more. This is not a monorepo — it's a flat collection of independent templates organized by category under `boilerplates/`.

## Commands

The primary task runner is [Taskfile](https://taskfile.dev/) (Go Task), not npm scripts (most npm scripts are TODO stubs).

```bash
# Setup
task bootstrap          # Install Homebrew and Python
task install            # Install deps from Brewfile and requirements.txt

# Validation & Fixing
task validate           # Run pre-commit hooks + ESLint + Prettier checks
task check              # ESLint + Prettier only
task fix                # Auto-fix ESLint + Prettier issues
task preCommit          # Run pre-commit hooks on all files

# Security
task security           # Run secret detection + SAST scans
task secrets            # Secret pattern detection (check_for_pattern.sh + Whispers)
task sast               # Snyk dependency + code scanning

# npm (limited — most scripts are TODO)
npm run check:eslint    # ESLint check
npm run check:prettier  # Prettier check
npm run fix             # ESLint + Prettier auto-fix
```

## Code Style & Formatting

- **Indentation** follows `.editorconfig`:
  - 2 spaces: JS, TS, JSON, CSS, HTML, YAML, Astro, Markdown
  - 4 spaces: Python, Dockerfile, Terraform, Bash scripts
  - Tabs: Makefiles
- **Python**: Formatted with Black via pre-commit
- **Shell**: Validated with ShellCheck (severity=error, excludes SC3037/SC2148)
- **Terraform**: `terraform fmt` + `terraform_docs` + Checkov via pre-commit
- **Ansible**: ansible-lint (skips yaml[truthy] and yaml[line-length])
- **Commits**: [Conventional Commits](https://www.conventionalcommits.org) format — `<type>[scope]: <description>`

## Pre-commit Hooks

Pre-commit is configured with `no-commit-to-branch` — direct commits to `main` are blocked. The hook suite also checks YAML/JSON/XML/TOML validity, detects private keys, enforces LF line endings, and runs all language-specific linters listed above.

## CI/CD (GitHub Actions)

- **PRs**: pre-commit hooks, ESLint, Prettier, security scans (Snyk + Whispers)
- **Merge to main**: Auto-bumps patch version via git tag and creates a GitHub release with generated notes

## Boilerplate Categories

Templates live under `boilerplates/` organized as: `ansible.md`, `appleScripts/`, `automationTemplates/` (n8n, Kestra, Trigger.dev), `docker/`, `scriptTemplates/` (Go, Python, Shell), `serverlessFunctionTemplates/` (AWS Lambda, GCP, Netlify), `webTemplates/`.
