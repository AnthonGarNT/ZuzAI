# Zuz AI

Zuz AI is a personal finance assistant that tracks your spending and keeps you honest about your budget.

It watches your bank or credit card transactions, asks you about each new purchase, and uses Claude to summarize your spending daily and monthly.

## Features

- **Transaction detection**: pulls new transactions from your bank or card provider through a pluggable connector (API, MCP server, or CSV import).
- **Purchase check-in**: when a new purchase appears, Zuz sends a push notification asking what it was and which budget it belongs to.
- **Daily summary**: after each day, a recap of what you spent, where, and how it affected your budgets.
- **Monthly summary**: did you stick to your budget, where did you overspend, how much did you save, and how does it compare to previous months.
- **Local-first**: data is stored in a local SQLite database. Only the minimum needed (amount, merchant, category, budget totals) is sent to the Claude API.

## How it works

1. A connector fetches new transactions.
2. Zuz notifies you and records your answer (purchase description + budget).
3. Claude generates daily and monthly summaries from your stored data.

## Status

Early development. Built with Claude Code.