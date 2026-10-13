---
description: Build the next feature, tests first, then open a pull request
---

# /build

1. Read AGENTS.md, SECURITY.md, API_CONTRACT.md, DESIGN.md.
2. Take the next unbuilt feature from FEATURES.md.
3. Create a git branch for it.
4. Write tests from its acceptance criteria first, including security and failure cases. Run them and show that they fail.
5. Write the minimum code to make them pass. Follow API_CONTRACT.md and DESIGN.md.
6. Never skip, delete, or weaken a test. Never add a dependency without asking.
7. Run lint, typecheck, unit tests, and e2e tests. Fix what fails.
8. Execute the [/verify](verify.md) workflow to run all checks and review the diff as a skeptic. Address any findings.
9. Commit using Conventional Commits (feat:, fix:, refactor:, chore:).
10. Push the branch and open a pull request, embedding the verification report in the summary.
11. Stop. Wait for my review. Do not start the next feature.
