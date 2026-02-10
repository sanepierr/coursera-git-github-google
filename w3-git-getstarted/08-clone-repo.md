# Clone a Repository

- Summary: `git clone` copies a remote repository to your local machine.
- Key points:
  - Cloning creates a full local copy with history and `origin` remote set.
  - To clone into a specific directory: `git clone <url> myfolder`.
- Example commands:
  - `git clone https://github.com/user/repo.git`
  - `cd repo`
  - `git remote -v` — verify `origin` remotes
- Forks + remotes:
  - When working with a fork, rename upstream: `git remote rename origin upstream` then add your fork as `origin`.
- Tip: After cloning, run `git status` and `git log` to inspect the repo state.