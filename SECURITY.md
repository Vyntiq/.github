# Security policy

## Reporting a vulnerability

Please report security issues privately to **info@vyntiq.co.in** with the subject line `SECURITY`.
Do not open a public issue.

Include what you found, how to reproduce it and its impact. We acknowledge reports within 2 working days and
keep you informed until the issue is fixed.

## For Vyntiq engineers

- Never commit secrets: passwords, tokens, private keys, connection strings or customer data. Every push to
  every Vyntiq repository is scanned automatically, and a finding marks the commit red.
- If a secret reaches a repository, **rotate it first**. Removing it from git does not make it safe again.
- Test fixtures that look like secrets can be allow-listed in the repository's `.gitleaks.toml`.
- Dependabot security alerts are on for every repository. Fix or dismiss them with a reason; don't leave them open.
