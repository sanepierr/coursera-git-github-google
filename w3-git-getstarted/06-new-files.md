# New Files

- Summary: How Git treats newly created files in your project.
- Key points:
  - New files are "untracked" until added to the staging area.
  - Use `git status` to view untracked files.
  - To start tracking: `git add <file>` then `git commit -m "message"`.
- Example commands:
  - `touch index.html` (or create a file in an editor)
  - `git status`
  - `git add index.html`
  - `git commit -m "Add index.html"`
- Tip: Save files in the correct project folder (`pwd`/`cd`) before running Git commands.