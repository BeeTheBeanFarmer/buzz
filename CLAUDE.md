# CLAUDE.md - AI Assistant Guide for Buzz Repository

> **Purpose**: This file provides AI assistants with comprehensive context about the Buzz repository, including codebase structure, development workflows, conventions, and best practices.

> **Last Updated**: 2026-01-17

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Repository Structure](#repository-structure)
3. [Technology Stack](#technology-stack)
4. [Development Workflow](#development-workflow)
5. [Code Conventions & Standards](#code-conventions--standards)
6. [Testing Guidelines](#testing-guidelines)
7. [Git Workflow](#git-workflow)
8. [Common Tasks & Commands](#common-tasks--commands)
9. [AI Assistant Guidelines](#ai-assistant-guidelines)
10. [Troubleshooting](#troubleshooting)

---

## Project Overview

### Project Name
**Buzz** (repository: BeeTheBeanFarmer/buzz)

### Description
> **Note**: This is a new repository. Project description to be added as development progresses.

### Key Objectives
- To be defined as project requirements are established

### Important Context
- Repository initialized: 2026-01-17
- This is a fresh project with no existing codebase
- Documentation will be updated as the project evolves

---

## Repository Structure

### Current State
This is a new repository. The directory structure will be documented here as it develops.

### Standard Directory Layout (Recommended)
When the project structure is established, it may follow a pattern like:

```
buzz/
├── src/                    # Source code
├── tests/                  # Test files
├── docs/                   # Documentation
├── config/                 # Configuration files
├── scripts/                # Build and utility scripts
├── .github/                # GitHub workflows and templates
├── README.md               # Project readme
├── CLAUDE.md               # This file
├── CONTRIBUTING.md         # Contribution guidelines (if applicable)
└── LICENSE                 # License file (if applicable)
```

**Note**: Update this section as the actual directory structure is created.

---

## Technology Stack

### Languages
> To be determined based on project requirements

### Frameworks & Libraries
> To be added as dependencies are introduced

### Development Tools
- **Version Control**: Git
- **Repository Host**: GitHub (BeeTheBeanFarmer/buzz)

### Build Tools
> To be added when build system is set up

---

## Development Workflow

### Branch Strategy

#### Main Branches
- **main/master**: Production-ready code (primary branch to be determined)

#### Feature Branches
- AI assistants develop on branches following pattern: `claude/claude-md-<session-id>`
- Example: `claude/claude-md-mkir6frvvdwlzf74-Z6TFe`
- These branches are automatically created for AI assistant sessions

#### Branch Naming Convention
For human developers (if applicable):
- Feature branches: `feature/<description>`
- Bug fixes: `bugfix/<description>`
- Hotfixes: `hotfix/<description>`

### Development Process

1. **Start Work**
   - AI assistants work on designated `claude/*` branches
   - Human developers create feature branches from main

2. **Make Changes**
   - Follow code conventions (see below)
   - Write tests for new functionality
   - Update documentation as needed

3. **Commit Changes**
   - Use clear, descriptive commit messages
   - Reference issues/tickets if applicable

4. **Push & Create PR**
   - Push to feature branch
   - Create Pull Request for review
   - Ensure all tests pass

5. **Code Review**
   - Address feedback
   - Merge when approved

---

## Code Conventions & Standards

### General Principles

1. **Clarity over Cleverness**: Write code that's easy to understand
2. **Consistency**: Follow established patterns in the codebase
3. **Simplicity**: Avoid over-engineering; implement only what's needed
4. **Documentation**: Comment complex logic; keep functions self-documenting

### Naming Conventions

> To be established based on chosen programming language

**General Guidelines**:
- Use descriptive, meaningful names
- Avoid abbreviations unless widely understood
- Be consistent with existing codebase patterns

### Code Style

> To be defined when primary language is chosen

**Recommended Practices**:
- Use a linter/formatter for consistent style
- Follow language-specific style guides (e.g., PEP 8 for Python, Google Style for JavaScript)
- Configure editor/IDE to match project standards

### Comments & Documentation

- **When to Comment**:
  - Complex algorithms or business logic
  - Non-obvious decisions or workarounds
  - Public APIs and interfaces
  - Edge cases or special handling

- **When NOT to Comment**:
  - Self-explanatory code
  - Obvious operations
  - Redundant information

### File Organization

- Keep files focused and reasonably sized
- Group related functionality together
- Separate concerns (business logic, UI, data access, etc.)

---

## Testing Guidelines

### Testing Strategy

> To be established when testing framework is chosen

**Recommended Approach**:
1. **Unit Tests**: Test individual functions/methods
2. **Integration Tests**: Test component interactions
3. **End-to-End Tests**: Test complete user workflows (if applicable)

### Test Location

> Update this section when test structure is established

**Common Patterns**:
- Tests alongside source files: `src/module.test.js`
- Separate test directory: `tests/` mirroring `src/` structure

### Writing Tests

**Best Practices**:
- Write tests for new features
- Update tests when modifying existing code
- Aim for meaningful coverage, not just high percentages
- Test edge cases and error conditions
- Keep tests independent and repeatable

### Running Tests

> Add test commands here when test framework is set up

```bash
# Example (to be replaced with actual commands):
# npm test
# pytest
# go test ./...
```

---

## Git Workflow

### Commit Message Format

Use clear, descriptive commit messages:

```
<type>: <subject>

<body (optional)>

<footer (optional)>
```

**Types**:
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, no logic changes)
- `refactor`: Code refactoring
- `test`: Adding or updating tests
- `chore`: Maintenance tasks

**Examples**:
```
feat: add user authentication system

fix: resolve null pointer exception in data processor

docs: update CLAUDE.md with testing guidelines
```

### Push Protocol

**For AI Assistants**:
- Always use: `git push -u origin <branch-name>`
- Branch must start with `claude/` and end with matching session ID
- If push fails due to network errors, retry up to 4 times with exponential backoff (2s, 4s, 8s, 16s)

**For All Developers**:
- Pull latest changes before pushing
- Resolve conflicts locally
- Never force push to main/protected branches without approval

### Pre-commit Checks

> To be added when pre-commit hooks are configured

**Recommended Checks**:
- Linting
- Formatting
- Test execution
- Security scanning

---

## Common Tasks & Commands

### Initial Setup

> Add setup instructions here when project structure is established

```bash
# Example (to be replaced with actual setup):
# git clone <repository-url>
# cd buzz
# <install dependencies>
# <configure environment>
```

### Development Commands

> Add common development commands here

```bash
# Examples (to be replaced):
# Start development server:
# npm start / python manage.py runserver / go run main.go

# Build project:
# npm run build / make build / cargo build

# Run tests:
# npm test / pytest / go test ./...

# Lint code:
# npm run lint / flake8 . / golangci-lint run
```

### Dependency Management

> Add dependency management instructions

```bash
# Examples (to be replaced):
# Add dependency:
# npm install <package> / pip install <package> / go get <package>

# Update dependencies:
# npm update / pip install -U -r requirements.txt / go get -u
```

---

## AI Assistant Guidelines

### Core Principles for AI Assistants

1. **Read Before Modifying**
   - ALWAYS read files before making changes
   - Understand existing code before suggesting modifications
   - Never propose changes to code you haven't seen

2. **Avoid Over-Engineering**
   - Only make changes that are directly requested or clearly necessary
   - Keep solutions simple and focused
   - Don't add features beyond what was asked
   - Don't add unnecessary abstractions, error handling, or future-proofing

3. **Code Quality**
   - Follow existing patterns in the codebase
   - Match the style and conventions already established
   - Don't refactor code unless specifically asked
   - Don't add comments to unchanged code

4. **Security Awareness**
   - Watch for common vulnerabilities (XSS, SQL injection, command injection, etc.)
   - Validate user input at system boundaries
   - Don't add unnecessary validation for internal code
   - Fix security issues immediately if discovered

5. **Testing**
   - Write tests for new features when applicable
   - Update tests when modifying existing code
   - Run tests before committing
   - Don't skip tests unless explicitly instructed

### Working with This Repository

1. **Branch Management**
   - You'll work on branches like `claude/claude-md-<session-id>`
   - Always develop on your designated branch
   - Never push to main without explicit permission

2. **Commit Strategy**
   - Make atomic commits (one logical change per commit)
   - Write clear commit messages following the format above
   - Commit after completing logical units of work

3. **Push Strategy**
   - Use `git push -u origin <branch-name>`
   - Retry on network failures (up to 4 times with exponential backoff)
   - Verify branch name follows required pattern

4. **Documentation**
   - Update CLAUDE.md when project structure changes significantly
   - Keep documentation current with code changes
   - Document new conventions or patterns as they're established

### Task Management

When working on complex tasks:

1. Use TodoWrite tool to plan and track progress
2. Break down large tasks into smaller steps
3. Mark tasks as in_progress before starting
4. Mark tasks as completed immediately after finishing
5. Keep only one task in_progress at a time

### Communication

- Be concise and clear in responses
- Use markdown for formatting
- Reference specific file locations with `file_path:line_number` format
- Don't use emojis unless explicitly requested
- Output text directly; don't use bash echo to communicate

---

## Troubleshooting

### Common Issues

> This section will be populated with common issues and solutions as they arise

#### Git Issues

**Problem**: Push fails with 403 error
- **Solution**: Verify branch name starts with `claude/` and ends with matching session ID

**Problem**: Network timeout during git operations
- **Solution**: Retry with exponential backoff (implemented automatically for AI assistants)

#### Build Issues

> To be added as build system is established

#### Runtime Issues

> To be added as application is developed

### Getting Help

- Check existing documentation in `docs/` (when available)
- Review issue tracker for known problems
- Examine recent commit history for similar changes
- Refer to framework/library documentation

---

## Maintenance & Updates

### Updating This Document

This document should be updated when:
- Project structure changes significantly
- New tools or frameworks are added
- Development workflow changes
- New conventions or patterns are established
- Common issues and solutions are discovered

### Document Ownership

- **Maintained by**: Development team and AI assistants
- **Review frequency**: As needed when project evolves
- **Update protocol**: Submit changes via Pull Request

---

## Appendix

### Quick Reference

**Repository**: BeeTheBeanFarmer/buzz
**Current Branch Pattern**: `claude/claude-md-<session-id>`
**Primary Language**: TBD
**Framework**: TBD
**Test Framework**: TBD

### Related Documentation

> Add links to related documentation here:
- README.md (when created)
- CONTRIBUTING.md (if applicable)
- API documentation (if applicable)
- Architecture decision records (if maintained)

### Change Log

| Date | Change | Updated By |
|------|--------|------------|
| 2026-01-17 | Initial creation of CLAUDE.md | AI Assistant |

---

**Note to AI Assistants**: This document is your primary reference for working with this repository. Keep it updated as the project evolves. When in doubt, refer to this guide and ask clarifying questions before making significant changes.
