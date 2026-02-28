# sirrlock/scoop-bucket

Scoop bucket for Sirr — the ephemeral secret manager (Windows).

## Install

```powershell
scoop bucket add sirrlock https://github.com/sirrlock/scoop-bucket
scoop install sirrlock/sirrd   # Server daemon
scoop install sirrlock/sirr    # CLI client
```

## Packages

| Package | Description |
|---------|-------------|
| `sirrd` | Sirr daemon — self-hosted secret vault server |
| `sirr`  | Sirr CLI — push, get, and manage secrets from the terminal |

## Mac/Linux

Use Homebrew: `brew tap sirrlock/tap`
