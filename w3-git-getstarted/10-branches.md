# Branches

- Summary: Branches are separate workspaces for features or fixes.
- Common commands:
  - `git branch` — list branches
  - `git branch <name>` — create a branch
  - `git checkout <name>` or `git switch <name>` — switch branches
  - `git checkout -b <name>` — create and switch
  - `git merge <branch>` — merge into current branch
  - `git branch -d <name>` — delete a merged branch
- Workflow tips:
  - Keep branches focused and short-lived
  - Regularly sync with `main` to avoid large merge conflicts
  - Use descriptive names: `feature/login`, `bugfix/issue-123`
- Example:
  - `git checkout -b feature/header`
  - make changes, `git add .`, `git commit -m "Add header"`
  - `git checkout main`, `git merge feature/header`