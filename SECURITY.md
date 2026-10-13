# SECURITY.md

## Rules
- Every endpoint checks who is asking AND whether they are allowed to access that specific item.
- All input is validated with a schema on the server. Never trust the browser.
- Database access only through parameterized queries or the ORM. No string-built SQL.
- Passwords hashed with a modern algorithm (argon2 or bcrypt). Never stored or logged in plain text.
- Secrets only in environment variables. Provide a .env.example, never a real .env.
- Output is escaped by default. No raw HTML injection.
- Sessions/cookies: HttpOnly, Secure, SameSite set.
- Rate-limit login and any expensive endpoint.
- Set security headers (CSP, X-Content-Type-Options, etc.).
- Errors shown to users never reveal internals.
- Log security events, never log secrets.

## Required tests
- User A cannot read, edit, or delete user B's data (test every resource type).
- Unauthenticated requests to protected routes are rejected.
- Invalid and malicious input is rejected (empty, huge, wrong type, script tags, SQL-like text).
- Rate limits actually trigger.

## Reference checklists
- OWASP Top 10: https://owasp.org/www-project-top-ten/
- OWASP Web Security Testing Guide: https://owasp.org/www-project-web-security-testing-guide/