# Project

## Setup

1. Clone the repository.
2. Install dependencies with the package manager used by this project.
3. Copy `.env.example` to `.env`.
4. Fill local environment variables in `.env`.

## Daily Workflow

Before editing:

```bash
git status
git pull --rebase
```

After editing:

```bash
git status
git add <files>
git commit -m "feat: describe change"
git push
```

Before switching computers, commit and push local work. On the next computer, pull before editing.

## Safety

Do not commit secrets, tokens, cookies, private configuration, sensitive logs, or local `.env` files.
