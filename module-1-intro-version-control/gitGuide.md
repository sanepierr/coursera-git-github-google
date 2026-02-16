**1. The Three Sections of a Git Project**

Every Git project has three main sections:

| Section           | Purpose                                                                      |
| ----------------- | ---------------------------------------------------------------------------- |
| **Git directory** | Stores the history of all files and changes (the “database” of the project). |
| **Working tree**  | The current version of your project where you make edits (like a sandbox).   |
| **Staging area**  | Contains changes marked to be committed next (also called the index).        |


2. Key Git Commands

| Command       | Purpose                                                               | Example                                                                                        |
| ------------- | --------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `git config`  | Sets your identity in Git (user.name and user.email)                  | `git config --global user.email "me@example.com"`<br>`git config --global user.name "My name"` |
| `git init`    | Creates a new empty repository or re-initializes one                  | `git init`                                                                                     |
| `ls -la`      | Lists all files (including hidden ones) in a directory                | `ls -la`                                                                                       |
| `ls -l .git/` | Shows the contents of the Git directory                               | `ls -l .git/`                                                                                  |
| `git add`     | Adds changes to the staging area                                      | `git add disk_usage.py`                                                                        |
| `git status`  | Shows current status of files (modified, staged, committed)           | `git status`                                                                                   |
| `git commit`  | Saves staged changes to the Git directory (requires a commit message) | `git commit` or `git commit -m "Add a check_reboot function"`                                  |

**3. Git Workflow: Modified → Staged → Committed**

Modified – You change a file in the working tree.

Staged – You mark the changes for commit using git add.

Committed – You save a snapshot to the Git directory using git commit.

**4. Writing Good Commit Messages Structure:**

Summary (first line)

Short (~50 characters), descriptive.

Acts like a header.

Description (body)

Kept under 72 characters per line.

Explains the “why” behind the change.

Can reference bugs, issues, tickets, or external links.

**5. Key Takeaways**

Git organizes your project into three sections for easy tracking.

Use git add to stage changes and git commit to record snapshots.

Writing clear commit messages improves communication and project maintainability.

Workflow: modify → stage → commit.