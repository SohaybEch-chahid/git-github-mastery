# GitHub CLI (`gh`) — Complete Guide

> The official GitHub command-line tool for Fedora users.

---

## What is `gh`?

`gh` is the **official GitHub CLI (Command Line Interface)** made by GitHub.  
It lets you interact with **GitHub as a platform** directly from your terminal — no browser needed.

### `git` vs `gh` — Key Difference

| | `git` | `gh` |
|---|---|---|
| **Purpose** | Version control (commits, branches, merges) | GitHub platform (PRs, issues, repos) |
| **Works with** | Any remote (GitHub, GitLab, etc.) | GitHub specifically |
| **Made by** | Linus Torvalds / community | GitHub (Microsoft) |
| **Example** | `git commit`, `git push` | `gh pr create`, `gh issue list` |

> 💡 Think of it this way:  
> **`git`** manages your **code**.  
> **`gh`** manages your **GitHub account and workflows**.

---

## Installation on Fedora

### Method 1 — DNF (Recommended)

```bash
sudo dnf install gh
```

### Method 2 — Official GitHub RPM Repository (Latest Version)

```bash
sudo dnf config-manager --add-repo https://cli.github.com/packages/rpm/gh-cli.repo
sudo dnf install gh
```

### Verify Installation

```bash
gh --version
```

---

## Authentication (Login)

```bash
gh auth login
```

You will be asked:
1. **GitHub.com** or GitHub Enterprise → choose `GitHub.com`
2. **HTTPS** or SSH → choose your preference
3. **Login with a web browser** or token → browser is easiest

### Check Login Status

```bash
gh auth status
```

---

## Core Commands

### 🗂️ Repositories

```bash
gh repo create my-project        # Create a new GitHub repo
gh repo clone username/repo      # Clone a repo
gh repo view                     # View repo info in terminal
gh repo list                     # List your repos
gh repo fork username/repo       # Fork a repo
```

### 🔀 Pull Requests

```bash
gh pr create                     # Open a new pull request
gh pr list                       # List open PRs
gh pr view 42                    # View details of PR #42
gh pr merge 42                   # Merge PR #42
gh pr review                     # Review a PR
gh pr checkout 42                # Switch to the branch of PR #42
```

### 🐛 Issues

```bash
gh issue create                  # Create a new issue
gh issue list                    # List all open issues
gh issue view 10                 # View issue #10
gh issue close 10                # Close issue #10
gh issue reopen 10               # Reopen a closed issue
```

### ⚙️ GitHub Actions (CI/CD)

```bash
gh run list                      # See all workflow runs
gh run view                      # View a specific run
gh run watch                     # Watch a run in real time
gh workflow list                 # List all workflows
gh workflow run deploy.yml       # Manually trigger a workflow
```

### 🔐 Authentication

```bash
gh auth login                    # Log in to GitHub
gh auth logout                   # Log out
gh auth status                   # Check login status
gh auth token                    # Show current token
```

---

## Common Workflow Example

Here's a typical day-to-day workflow using both `git` and `gh`:

```bash
# 1. Clone a repo
gh repo clone username/my-project

# 2. Create a new branch and make changes
cd my-project
git checkout -b feature/my-feature
# ... make your edits ...

# 3. Stage and commit
git add .
git commit -m "Add new feature"

# 4. Push the branch
git push origin feature/my-feature

# 5. Open a Pull Request directly from terminal
gh pr create --title "Add new feature" --body "Description of the feature"

# 6. Check PR status later
gh pr list

# 7. Merge when ready
gh pr merge --squash
```

---

## Useful Flags & Tips

```bash
# Create a PR and open it in the browser
gh pr create --web

# Create a private repo
gh repo create my-project --private

# Create issue with a title directly
gh issue create --title "Bug: login fails" --body "Steps to reproduce..."

# View output in the browser
gh repo view --web
gh issue view 5 --web
gh pr view 3 --web
```

---

## Why Use `gh`?

- ✅ Stay in the terminal — no context switching to the browser
- ✅ Automate GitHub workflows with scripts
- ✅ Faster PR and issue management
- ✅ Works great with GitHub Actions pipelines
- ✅ Pairs perfectly with `git` for a full developer workflow

---

## Resources

- 📖 Official Docs: [cli.github.com/manual](https://cli.github.com/manual)
- 💻 GitHub Repo: [github.com/cli/cli](https://github.com/cli/cli)
- 🔍 Help in terminal: `gh help` or `gh <command> --help`
