# Anatomy of a Commit Message

## Overview

A commit message explains **why a change was made** and provides context for future developers (including future you!). Clear commit messages save time when debugging or reviewing project history.

---

## Structure of a Good Commit Message

1. **Summary line (first line)**  
   - Short and descriptive (~50 characters).  
   - Summarizes the main purpose of the commit.  
   - Example: `Add a check_reboot function`.

2. **Blank line**  
   - Separates the summary from the body.

3. **Body (optional but recommended)**  
   - Provides detailed explanation of the change.  
   - Lines are kept under 72 characters for readability.  
   - Can reference related issues, bugs, or tickets.  
   - Example:  
     ```
     The purpose of this commit is to add a function that checks
     if the computer requires a reboot. This will help scripts
     avoid performing operations when a reboot is pending.
     ```

---

## Tips for Writing Commit Messages

- Keep **audience in mind**: future you or other developers.  
- Avoid vague messages like `update` or `fix`.  
- Include context about **why** a change was made.  
- Reference external information (design docs, tickets, bug reports) when helpful.  
- Stick to line length limits (50 chars for the summary, 72 for the body) for readability.

---

## Viewing Commit History

Use the command:

```bash
git log
```

```
commit d8e139cc4f7dcd13b75cff67cfb68527e24c59c5 (HEAD -> master)
Author: My name <me@example.com>
Date:   Thu Jul 11 17:19:32 2019 +0200

    Add a check_reboot function

commit 6cfc29966acda8213fcd8ac2735b31f3fdbc6c53
Author: My name <me@example.com>
Date:   Thu Jul 11 12:08:46 2019 +0200

    Create an empty all_checks.py

```

**What git log shows for each commit:**

Commit hash – unique identifier.

HEAD and branch – where the commit is located in the branch.

Author name and email – who made the commit.

Date and time – when the commit occurred.

Commit message – summary of changes.
