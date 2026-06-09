# SSH Authentication

## Generate Key

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

## Start Agent

```bash
eval "$(ssh-agent -s)"
```

## Add Key

```bash
ssh-add ~/.ssh/id_ed25519
```

## Test Connection

```bash
ssh -T git@github.com
```
