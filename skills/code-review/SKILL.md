---
name: code-review
description: Reviews code changes using CodeRabbit AI. Use when user asks for code review, PR feedback, code quality checks, security issues, or wants autonomous fix-review cycles.
---

# CodeRabbit Code Review

AI-powered code review using CodeRabbit. Enables autonomous development workflows where you can implement features, review code, and fix issues without manual intervention.

## When to Use

When user asks to:

- Review code changes / Review my code / Review this
- Check code quality / Code quality check
- Find bugs or security issues / Check for bugs / Find issues
- Security review / Security check
- Get feedback on their code / PR review / Pull request feedback
- Review staged/uncommitted changes
- What's wrong with my code / What's wrong with my changes
- Run coderabbit / Use coderabbit
- Implement a feature and review it
- Fix issues found in review

## How to Review

### 1. Check Prerequisites

```bash
# Check CLI
coderabbit --version 2>/dev/null

# Check auth
coderabbit auth status 2>&1
```

**If CLI not installed**, tell user:

```bash
Please install CodeRabbit CLI first:
curl -fsSL https://cli.coderabbit.ai/install.sh | sh
```

**If not authenticated**, tell user:

```bash
Please authenticate first by running in your terminal:
coderabbit auth login
```

### 2. Run Review

```bash
coderabbit review --plain
```

Options:

- `-t all` - All changes (default)
- `-t committed` - Committed changes only
- `-t uncommitted` - Uncommitted changes only
- `--base main` - Compare against specific branch

### 3. Present Results

Group findings by severity and create a task list for issues found.

### 4. Fix Issues (Autonomous Workflow)

When user requests implementation + review:

1. Implement the requested feature
2. Run `coderabbit review --plain`
3. Create task list from findings
4. Systematically fix each issue
5. Re-run review if needed until critical issues resolved

## Documentation

For more details: <https://docs.coderabbit.ai/cli/claude-code-integration>
