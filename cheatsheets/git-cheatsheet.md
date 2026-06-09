# Git Cheat Sheet

## Repository

```bash
git init
git clone URL
```

## Status

```bash
git status
```

## Staging

```bash
git add file.txt
git add .
```

## Commit

```bash
git commit -m "message"
```

## History

```bash
git log
git log --oneline
```

## Branches

```bash
git branch
git branch branch-name
git switch branch-name
git switch -c branch-name
```

## Merge

```bash
git merge branch-name
```

## Remote

```bash
git remote -v
git remote add origin URL
```

## Push & Pull

```bash
git push
git pull
git fetch
```

## Stash

```bash
git stash
git stash pop
```

## Undo

```bash
git restore file.txt
git reset
git revert COMMIT_HASH
```

## Tags

```bash
git tag v1.0
git push origin v1.0
```
