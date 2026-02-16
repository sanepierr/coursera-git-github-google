# The Basic Git Workflow

## Overview

A typical Git workflow involves **creating a repository, adding files, and committing changes**. Every repository has three main areas:

1. **Git directory** – stores snapshots (history) of files.
2. **Working tree** – current version of your project files.
3. **Staging area** – holds changes that are ready to be committed.

---

## Initial Setup

1. **Create a new directory and initialize a Git repository:**

```bash
mkdir scripts
cd scripts
git init
```
Output confirms the repository is initialized:

```
Initialized empty Git repository in /home/user/scripts/.git/
```

**Check Git configuration:**

```
git config -l
```

**Important info includes and appears in public commit logs:**

```
user.email=me@example.com
user.name=My name
```

**Creating and Tracking a New File**

Create a new Python script:

```#!/usr/bin/env python3

def main():
    pass

main()
```


**Make the script executable:**

```
chmod +x all_checks.py
```


**Check repository status:**

```
git status
```


Output shows the file is untracked:

```
Untracked files:
  all_checks.py
  ```


**Stage the file:**

```
git add all_checks.py
git status
```


**File is now in the staging area. Commit the file:**

```
git commit
```


Launches a text editor (Nano by default) to enter a commit message.

Save and exit to create a snapshot.

