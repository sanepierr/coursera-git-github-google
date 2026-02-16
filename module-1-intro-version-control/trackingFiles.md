# Tracking Files with Git

## Overview

A Git project has **three main sections**:

1. **Git directory** – stores the history of all files and changes.
2. **Working tree** – contains the current state of your project.
3. **Staging area** – holds changes that are ready to be committed.

Think of Git as a series of snapshots. Each commit is a snapshot of your files at a specific point in time.

---

## File States

Each tracked file in Git can be in **one of three states**:

| State     | Description |
|-----------|-------------|
| Modified  | File has changes, but they are not yet staged. |
| Staged    | File is ready to be committed. |
| Committed | File changes are safely stored in a snapshot in the Git directory. |

---

## Example Workflow

1. **Check the current working tree and status**:

```bash
cd checks
ls -l
git status
```

**Edit a file:**

```
atom disk_usage.py
```

**Check status again:**

```
git status
```
Output will show the file as modified.

**Stage the file:**

```
git add disk_usage.py
git status
```
The file is now in the staging area.

**Commit the changes:**

```
git commit -m 'Add periods to the end of sentences.'
```
Git creates a snapshot in the Git directory and shows stats for the change.

**Check status one last time:**
```
git status
```
Output shows: nothing to commit, working tree clean.

