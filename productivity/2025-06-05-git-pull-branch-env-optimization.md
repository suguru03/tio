# Streamlining Git Pull with Branch Environment Variables

**Date:** 2025-06-05
**Category:** productivity

> 🇨🇦 [日本語版はこちら](./2025-06-05-git-pull-branch-env-optimization.ja.md)

## What I optimized
Eliminated the mental overhead of remembering different default branch names (dev, main, etc.) when running `git pull --rebase` across multiple projects by using environment variables. This also enables quick command retrieval via Ctrl+R terminal history search with consistent command format.

## How I did it
- Set up `.envrc` files in project directories to define the default branch
- Used `direnv` to automatically load branch configuration per project
- Configured `git pull --rebase $BRANCH` as a standard command
- For local-only settings, created local `.envrc` and added it to `.git/info/exclude`
- Used `source_up` to inherit parent directory configurations when needed

Example `.envrc` configuration:
```sh
source_up
export BRANCH=main
```

## Impact
- Removes decision fatigue when switching between projects with different default branches
- Prevents errors from pulling the wrong branch
- Standardizes git workflow across all projects
- Saves mental energy for more important development decisions
- Creates consistent muscle memory for git operations
- Enables instant command access via Ctrl+R terminal history search

## Lessons learned
- Environment variables can solve context-switching problems in development workflows
- Small cognitive loads add up across multiple daily operations
- Standardizing commands reduces mental overhead and prevents mistakes
- Project-specific configurations should be automated rather than memorized
