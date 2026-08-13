# Security policy

## Portfolio scope

This is a sanitized architecture and documentation repository. It is not the production system and must not contain production secrets or private records.

## Never commit

- API keys, passwords, authentication tokens, cookies, or recovery codes
- Account, project, agent, webhook, phone, or database identifiers
- Environment files containing real values
- Caller information, recordings, transcripts, or interaction records
- Private résumés, applications, employer communications, or calendar data
- Analytics exports, billing details, or production logs
- Medical, legal, disability, financial, government-ID, or precise-location data

## Reporting a security concern

Do not open a public issue containing vulnerability details or private information. Report concerns through the professional contact channel published on the owner's official website.

## Security principles

- Least privilege
- Server-side secret storage
- Signed event verification
- Replay protection and idempotency
- Input validation and output sanitization
- Human approval for consequential actions
- Data minimization and defined retention
- Untrusted-content and prompt-injection resistance
- Cost and abuse monitoring

