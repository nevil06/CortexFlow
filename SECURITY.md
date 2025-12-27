# Security Policy

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 1.x     | :white_check_mark: |

## Design Considerations

CortexFlow is designed for **local use only**:

- HTTP server binds to `localhost` (127.0.0.1)
- No built-in authentication (local trust model)
- Data stored locally in `~/.cortexflow/data/`

**Do NOT expose CortexFlow directly to the internet.** If remote access is needed, use a reverse proxy with proper authentication.

## Reporting a Vulnerability

If you discover a security vulnerability:

1. **Do NOT open a public issue**
2. Email **mithungowda.b7411@gmail.com** privately
3. Include:
   - Description of the vulnerability
   - Steps to reproduce
   - Potential impact
   - Suggested fix (if any)

We will:
- Acknowledge receipt within 48 hours
- Investigate and provide updates
- Credit reporters in security advisories (unless anonymity requested)

## Best Practices

When using CortexFlow:

- Keep Node.js updated
- Don't store sensitive data in project contexts
- Use firewall rules to restrict access
- Review project data periodically
- Run with minimal permissions

## Known Limitations

- No encryption at rest (local JSON files)
- No authentication/authorization
- No audit logging
- Designed for single-user local development
