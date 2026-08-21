# sirrlock/scoop-bucket — Claude Development Guide

## Purpose

Scoop bucket for Sirr on Windows. Provides two manifests: `sirrd` (server daemon) and `sirr` (CLI client).

```powershell
scoop bucket add sirrlock https://github.com/sirrlock/scoop-bucket
scoop install sirrlock/sirrd
scoop install sirrlock/sirr
```

## Structure

```
bucket/
├── sirrd.json    # sirrd server daemon manifest
└── sirr.json     # sirr CLI client manifest
```

## Updating on Release

When a new version of `sirr` / `sirrd` is released:

1. Update `version`
2. Update `url` to the new `.zip` release asset (Windows x86_64)
3. Update `hash` — `sha256:` prefix required (e.g. `sha256:abc123...`)
4. Commit and push

## Key Rules

- Scoop manifests use `sha256:` prefix on the hash field
- URL must point to a `.zip` Windows binary from the GitHub release
- `sirrd.json` and `sirr.json` are updated independently
- The release CI in `sirrlock/sirr` updates these manifests automatically via `SIRR_PACKAGE_MANAGERS_KEY`

## Pre-Commit Checklist

1. Are both hashes correct (`sha256:` prefix, correct value)?
2. Do both manifests reference the same version?

## Commit Attribution

**Never attribute commits to Claude, Anthropic, or any AI assistant.** This applies to every
commit in this repo, with no exceptions:

- Do **not** add `Co-Authored-By: Claude` (or any AI/assistant) trailers.
- Do **not** add "Generated with Claude Code", robot badges, or `claude.ai/code` session links.
- Do **not** set the commit author or committer to Claude/Anthropic — commits are authored by
  the human maintainer only.

Commit messages describe the change, nothing else. No AI attribution in any form.
