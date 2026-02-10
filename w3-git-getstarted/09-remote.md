# Remote Repositories

- Summary: Remotes link your local repo to hosted repositories (e.g., GitHub).
- Common commands:
  - `git remote -v` — list remotes
  - `git remote add origin <url>` — add a remote
  - `git push -u origin main` — push and set upstream
- Fork workflow:
  - Rename original origin to `upstream`: `git remote rename origin upstream`
  - Add your fork as `origin`: `git remote add origin <your-fork-url>`
- Tip: Use meaningful remote names (origin, upstream) and keep them configured correctly.