---
name: commit
description: Add all changes, commit with auto-generated or custom message, and push to remote repository
---

# Commit and Push Changes

This command will:
1. Add all changed files to git
2. Create a commit with an auto-generated message (or use your custom message)
3. Push the commit to the remote repository

## Usage

```
/commit                    # Auto-generates commit message
/commit "Your message"     # Uses your custom message
```

## What it does

1. Runs `git add -A` to stage all changes
2. If no message provided:
   - Quickly analyzes changed files using `git diff --staged --stat` and `git status --porcelain`
   - Generates a concise commit message based on the changes
3. Creates a commit with the message
4. Pushes to the current branch's remote

## Auto-generated Message Format

The auto-generated messages follow conventional commit style:
- `feat:` for new features
- `fix:` for bug fixes
- `docs:` for documentation changes
- `refactor:` for code refactoring
- `chore:` for maintenance tasks
- `init:` for initial commits

## Examples

```
/commit
# Might generate: "feat: add user authentication module"

/commit "fix: resolve login validation issue"
# Uses your provided message
```

## Notes

- Auto-generation is fast and uses minimal tokens by analyzing file statistics only
- Make sure you have a clean working directory before running
- The command will use the current branch for pushing
- Ensure you have push permissions to the remote repository