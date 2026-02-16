# First Steps with Git

## Configuring Git

Before we start using Git, we need to tell it who we are so it can track who makes changes.

```bash
git config --global user.email "me@example.com"
git config --global user.name "My Name"
```

**Creating a Repository**

There are two ways to start a Git repository:

From scratch: Create a new directory and initialize Git.

Clone: Copy an existing repository from somewhere else.

```
mkdir example
cd example
git example
```

This creates a hidden .git directory, which acts as a database for your project.

```
ls -la
ls -l .git/
```

**Working Tree**

The working tree is the current version of your project where you modify files. New files are initially untracked by Git.

```
cp ../disk_usage.py .
ls -l
```

**Staging Changes**

To track a file, add it to the staging area:

```
git add disk_usage.py
git status
```

**Committing Changes**
```
git commit
```

