# Password gate audit — 2026-06-12

## Implemented protection

The opening screen is now protected by two sequential requirements:

1. A client-side SHA-256 password check.
2. Mandatory GDPR / data-processing / AI-use acceptance.

The questionnaire opens only when both conditions are completed.

## Password handling

- The plain password is not stored in the HTML.
- The plain password is not submitted with the form.
- The HTML contains only the SHA-256 hash of the access password.
- Successful password verification is stored only for the current browser session where available (`sessionStorage`).
- A fallback to `localStorage` is used only if the browser does not allow session storage.

## Submitted audit metadata

The form records:

- password gate verification timestamp;
- GDPR / AI notice acceptance timestamp;
- acceptance language;
- notice version;
- acceptance text snapshot;
- browser/user-agent metadata.

It does not record the actual password.

## Important security limitation

This is a static front-end password gate suitable for controlled client-access friction, not a real server-side authentication layer. A technically skilled person could still inspect or bypass static front-end logic. For true access control, the page should be placed behind server-side authentication, HTTP Basic Auth, a protected reverse proxy, Cloudflare Access, Netlify/Vercel password protection, or similar.

## Recommendation

For the current use case — a non-indexed client questionnaire with legal acceptance and a private access password — this implementation is appropriate as a front-end protection layer. For confidential trade secrets or sensitive personal data, use server-side authentication instead.
