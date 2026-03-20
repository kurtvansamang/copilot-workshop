---
description: 'OWASP and security standards for all code'
applyTo: '**'
---

# Security Standards

- Validate all inputs server-side — never rely on client-side validation alone
- Sanitize data before rendering (Angular does this by default; never bypass with `bypassSecurityTrustHtml`)
- Wrap `JSON.parse()` calls in try/catch blocks
- Never store sensitive data in localStorage without encryption
- Apply input length limits on all text fields
- Use strict TypeScript types — no `any`
