---
description: Run every check, review the diff like a skeptic, and report
---

# /verify

1. Run lint, typecheck, unit tests, e2e tests (including the accessibility checks), npm audit, and the secret and Semgrep scans if they can run locally.
2. Check that every acceptance criterion in FEATURES.md has a test that would fail if the feature broke.
3. Review the whole diff against main as a skeptic. Look for:
   - skipped, deleted, or weakened tests
   - hard-coded secrets, keys, or URLs
   - endpoints missing a permission check
   - input that is not validated on the server
   - unused or unfamiliar dependencies
   - files changed that are unrelated to the feature
   - UI that breaks DESIGN.md or uses values outside styles/tokens.css
4. Write a report: what passed, what failed, what is risky.
5. If a preview deploy is set up, deploy it and give me the link. If not, build the app, start it locally, and tell me the address.
6. Do not fix anything in this step. Only report.
