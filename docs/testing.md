# Validation and testing plan

## Privacy tests

- Scan public artifacts for personal email addresses, telephone numbers, home locations, account IDs, and secrets
- Confirm fictional sample data contains no real people or employers
- Confirm public résumé excludes private contact information
- Confirm logs and errors do not expose user input or credentials

## Security tests

- Reject unsigned, invalid, stale, and replayed webhook events
- Deduplicate repeated event and call identifiers
- Validate same-origin and request-size protections
- Confirm secrets remain server-side
- Exercise rate limits and safe failure messages
- Test prompt-injection and malicious-link handling

## Workflow tests

- Require approval before applications, messages, scheduling, or commitments
- Confirm only authorized calendar and connector scopes are used
- Confirm one sanitized record is created for one approved interaction
- Confirm external content cannot alter policy
- Confirm unsupported actions fail closed

## Accessibility and experience tests

- Keyboard navigation and visible focus
- Mobile and desktop layouts
- Screen-reader labels and dialog behavior
- Clear AI disclosures and privacy notices
- Résumé page navigation and document-viewer close behavior

## Cost and abuse tests

- Usage alerts and conservative limits
- Duplicate-request suppression
- Bot, spam, repeated-caller, and appointment-abuse review
- No automatic purchases or expanded billing authority

