# git checkout

## Purpose

Older command used to switch branches and restore files.

## Switch Branch

```bash
git checkout main
```

## Create And Switch Branch

```bash
git checkout -b feature-login
```

## Restore File

```bash
git checkout -- file.txt
```

## Modern Alternative

Git introduced:

```bash
git switch
git restore
```

These are easier to understand and are generally preferred.

## Notes

Many projects still use checkout, so it is important to know.
```
