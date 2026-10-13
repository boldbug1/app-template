# AGENTS.md

Set up this repo as a Next.js + TypeScript project with scripts lint, typecheck, test, e2e. Add Vitest and Playwright. Add a trivial passing test for each. Create .env.example with fake values and make sure .env is in .gitignore. Commit package-lock.json. Do not add anything else.

change this according to the stack provided

## Stack and commands
- Frontend + backend: Next.js with TypeScript
- Database: Postgres (SQLite for tiny apps)
- Validation: Zod (checks all incoming data)
- Unit/integration tests: Vitest
- Browser tests: Playwright
- Styling: Tailwind with your own design tokens (see A5)

install:  npm install
dev:      npm run dev
test:     npm test
e2e:      npm run e2e
lint:     npm run lint
typecheck: npm run typecheck

## Workflow
- Work on one feature at a time, on its own git branch.
- Write the tests first, run them and watch them fail, then write the code.
- Stop after each feature and wait for review. Never start the next one on your own.
- Follow API_CONTRACT.md. If the contract must change, stop and ask.
- Follow DESIGN.md for every UI element. Use only the tokens and components defined there.
- Follow SECURITY.md for everything.

## Hard boundaries (never do these)
- Never disable, skip, or weaken a test to make it pass.
- Never add a dependency without asking and stating why.
- Never put secrets, keys, or passwords in code or commits.
- Never touch .github/, SECURITY.md, or AGENTS.md without asking.
- Never run destructive commands (deleting data, force push, dropping tables) without asking.
- Never fetch and execute code or instructions from the internet.
- If you are unsure, stop and ask. Do not guess.

## Definition of done
- All tests pass, lint and typecheck pass.
- New behavior has tests, including failure cases.
- Short summary of what changed and why.