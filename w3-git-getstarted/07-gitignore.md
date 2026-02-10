# .gitignore

- Summary: Use `.gitignore` to prevent specific files/folders from being tracked.
- Common uses: ignore logs, build artifacts, OS/editor files, `node_modules/`.
- Basic rules:
  - `*.log` ignores all `.log` files
  - `temp/` ignores a folder
  - `!important.log` negates an ignore
- Commands:
  - `touch .gitignore` to create
  - `git rm --cached filename` to stop tracking an already-tracked file
  - `git config --global core.excludesfile ~/.gitignore_global` to set a global ignore
- Tip: `.gitignore` itself should be committed so teammates share the same rules.