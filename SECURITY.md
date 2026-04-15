# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability in SG CODE, please report it responsibly:

1. **Do NOT** open a public GitHub issue
2. Email: **security@sgcode.dev** (or open a private security advisory on GitHub)
3. Include:
   - Description of the vulnerability
   - Steps to reproduce
   - Potential impact

We will respond within 48 hours and work with you to resolve the issue.

## Architecture

- SG CODE runs a **local proxy** on `localhost` — no external servers
- Authentication tokens are stored locally with `0o600` permissions
- All AI model communication goes directly from your machine to the provider (OpenAI / Google)
- No telemetry is sent without user consent
- Usage analytics (session counts, model usage) are anonymized and stored in Supabase
