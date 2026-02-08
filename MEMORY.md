# MEMORY.md - Nagesh's Preferences

## GitHub
- All projects created using **coding-agent** must be **private** by default

## Twitter/X (Bird Skill)
- Use bird **only for reading** tweets, searches, mentions, timelines
- **Never send tweets** without explicit user confirmation first

## Coding Projects
- Base directory for all Codex/coding-agent projects: **~/project/**
- Create subdirectories inside ~/project for each new project (e.g., ~/project/todo-app/, ~/project/my-app/)
- Never run Codex in ~/clawd/ or other system directories

## Project Setup Best Practices

### .gitignore
- Create a **decent default .gitignore** for any git project
- Include: Python bytecode, venv/, .env, .vscode/, IDE files, build artifacts, cache folders

### Environment Variables
- Use **`.env.example`** template pattern for configuration
- Only create env vars for values that may change per environment (paths, API keys, etc.)
- Don't over-engineer: only add env vars when actually needed
- Load `.env` with `python-dotenv` for local development
- Never commit actual `.env` files or secrets
