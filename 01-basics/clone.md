# git clone

## Purpose

Create a local copy of a remote repository.

## Syntax

```bash
git clone <repository-url>
```

## Example

```bash
git clone https://github.com/username/project.git
```

## What Happens?

- Downloads the repository.
- Downloads all branches and commits.
- Creates a local working directory.
- Automatically connects to the remote repository.

## Verify

```bash
git remote -v
```

## Notes

- Usually the first command used when working on an existing project.
- Creates the folder automatically.
```
