# Repository security

## Objective
Prevent accidental disclosure and reduce CI supply-chain exposure in this public learning repository.

## Controls
- .gitignore excludes common VM images, raw captures and sensitive configuration files. It does not protect already tracked files or all possible secrets.
- GitHub Actions secret scanning is configured on pushes, pull requests and manual runs. Actions are pinned to full commit SHAs resolved from upstream tags. Checkout uses read-only permissions, full history and no persisted credentials. PR comments and artifact uploads are disabled.
- CI scanning occurs after upload and is not a preventive push barrier. Full-history checkout does not itself guarantee every commit is scanned by every event.
- Local Gitleaks staged scanning and a pre-commit hook must be installed and tested in the local clone.
- Initial full-history scan, CI run verification, GitHub secret scanning/push protection and branch protection are pending.
- Review all public content before pushing. Never use real credentials to test detection. If a secret is exposed, revoke or rotate it immediately.

## Validation
Workflow committed; successful execution not yet confirmed. Branch main was unprotected and no rulesets were present at initial audit. Do not claim protection until verified.

## References
- [Gitleaks](https://github.com/gitleaks/gitleaks)
- [Gitleaks Action](https://github.com/gitleaks/gitleaks-action)
- [Git hooks](https://git-scm.com/docs/githooks)
- [GitHub Actions security](https://docs.github.com/en/actions/security-for-github-actions/security-guides/security-hardening-for-github-actions)
