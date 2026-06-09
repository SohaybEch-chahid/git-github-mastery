# git reset vs git revert

## git reset

Moves HEAD backward.

```bash
git reset --hard HEAD~1
```

## git revert

Creates a new commit that undoes changes.

```bash
git revert COMMIT_HASH
```

## Recommendation

Use `revert` when working with shared repositories.
