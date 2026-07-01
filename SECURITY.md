# Security Policy

## Supported Versions

| Version | Supported          |
|---------|--------------------|
| 0.0.x   | :white_check_mark: |

## Reporting a Vulnerability

If you discover a security vulnerability, please report it responsibly.

**Do NOT open a public issue for security vulnerabilities.**

### How to Report

1. **GitHub DM**: Send a direct message to [@minhphu102003](https://github.com/minhphu102003)
2. **Email**: Contact via GitHub profile email

### What to Include

- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Suggested fix (if any)

### Response Timeline

- **Acknowledgment**: Within 48 hours
- **Initial assessment**: Within 1 week
- **Fix release**: Depends on severity (critical issues within days, others in next release)

## Security Considerations

This action:

- Uses `contents: read` and `pull-requests: write` permissions only
- Passes all user inputs through environment variables (never inline in shell)
- Validates API responses before processing
- Does not store or log API keys
- Uses HTTPS for all API calls

### Known Risks

- **LLM output**: The action posts raw LLM output as PR comments. While `@mentions` are sanitized, prompt injection through diff content is theoretically possible.
- **API keys**: Users should use GitHub Secrets for all API keys, never hardcode them.
