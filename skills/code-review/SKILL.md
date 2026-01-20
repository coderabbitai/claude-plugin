---
name: code-review
description: Reviews code changes using CodeRabbit AI. Use when user asks for code review, PR feedback, or code quality checks.
---

# CodeRabbit Code Review

AI-powered code review using CodeRabbit.

## When to Use

When user asks to:
- Review code changes
- Check code quality
- Find bugs or security issues
- Get feedback on their code

## How to Review

### 1. Check Prerequisites

```bash
# Check CLI
coderabbit --version 2>/dev/null

# Check auth
coderabbit auth status 2>&1
```

**If CLI not installed**, tell user:
```
Please install CodeRabbit CLI first:
curl -fsSL https://cli.coderabbit.ai/install.sh | sh
```

**If not authenticated**, tell user:
```
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
- `--base main` - Compare against branch

### 3. Present Results

Group by severity and offer to apply fixes if available.
