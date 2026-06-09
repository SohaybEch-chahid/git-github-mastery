# Feature Branch Workflow

## Purpose

Develop features independently without affecting the main branch.

## Workflow

Create branch:

```bash
git switch -c feature-login
```

Develop feature.

Commit changes:

```bash
git add .
git commit -m "Add login page"
```

Push branch:

```bash
git push origin feature-login
```

Create Pull Request.

Merge into main.

## Advantages

- Cleaner history
- Safer development
- Easier reviews
