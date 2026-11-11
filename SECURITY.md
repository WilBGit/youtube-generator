# Security Policy

## Repository boundary

This repository contains source code and planning documentation for local video generation. It does not contain provider credentials, browser sessions, upload tokens, payment data, generated media, or publishing state.

## Prohibited content

Never commit API keys, TTS credentials, YouTube or Google OAuth files, social-media tokens, cookies, passwords, payment details, webhook URLs, private keys, `.env` files, generated media, or raw personal data.

## Credential handling

Configure providers through a local secret manager or environment variables. Keep local secret-bearing files owner-readable only. Use empty placeholders in examples. Do not put secrets in scripts, screenshots, issue reports, test data, or commit messages.

## Pre-push checklist

- Inspect staged names and file contents.
- Run `git diff --cached --check`.
- Scan current files and reachable history for high-confidence secret formats.
- Compile the generator and run a help or dry-run command without provider credentials.
- Verify generated output remains outside the repository.

If a credential is ever committed, revoke or rotate it immediately, remove it from current files and reachable history, and re-scan the remote repository.
