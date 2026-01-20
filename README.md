# CodeRabbit Plugin for Claude Code

AI-powered code review in Claude Code, powered by [CodeRabbit](https://coderabbit.ai).

## Installation

### 1. Prerequisites

Install and authenticate the CodeRabbit CLI:

```bash
curl -fsSL https://cli.coderabbit.ai/install.sh | sh
coderabbit auth login
```

### 2. Install Plugin

In Claude Code:

```bash
/plugin marketplace add coderabbitai/claude-plugin
/plugin install review@coderabbit
```

Or via CLI:

```bash
claude plugin marketplace add coderabbitai/claude-plugin
claude plugin install review@coderabbit
```

## Usage

```bash
/coderabbit:review
```

The command will:

- Verify CLI installation and authentication
- Run the code review
- Present findings grouped by severity

### Options

```bash
/coderabbit:review                    # Review all changes
/coderabbit:review committed          # Only committed changes
/coderabbit:review uncommitted        # Only uncommitted changes
/coderabbit:review --base main        # Compare against main
```

### Natural Language

You can also just ask Claude:

- "Review my code"
- "Check for security issues"
- "What's wrong with my changes?"

## Resources

- [CodeRabbit Documentation](https://coderabbit.ai/docs)
- [CodeRabbit CLI Guide](https://docs.coderabbit.ai/cli/overview)

## License

MIT
