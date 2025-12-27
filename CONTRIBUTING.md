# Contributing to CortexFlow

Thanks for your interest in contributing!

## Quick Start

```bash
git clone https://github.com/mithun50/CortexFlow
cd cortexflow
npm install
npm run dev
```

## Development

```bash
npm run dev          # Run with hot reload
npm run build        # Compile TypeScript
npm run test         # Run tests
npm run lint         # Check code style
```

## How to Contribute

### Bug Reports

Open an issue with:
- Clear description of the bug
- Steps to reproduce
- Expected vs actual behavior
- Environment details (OS, Node version, AI client)

### Feature Requests

Open an issue describing:
- The problem you're solving
- Your proposed solution
- Any alternatives considered

### Pull Requests

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/my-feature`
3. Make your changes
4. Run tests: `npm test`
5. Run linter: `npm run lint`
6. Commit with clear message: `git commit -m "Add: feature description"`
7. Push: `git push origin feature/my-feature`
8. Open a Pull Request

### Commit Messages

Use clear, descriptive commit messages:
- `Add: new feature`
- `Fix: bug description`
- `Update: changed functionality`
- `Docs: documentation changes`
- `Refactor: code improvements`

## Code Style

- TypeScript with strict mode
- ESLint for linting
- Meaningful variable names
- Comments for complex logic only

## Project Structure

```
src/
├── models.ts       # Data types and Zod schemas
├── storage.ts      # File-based persistence
├── server.ts       # MCP server implementation
├── http-server.ts  # REST API server
└── index.ts        # Entry point
```

## Testing

```bash
npm test              # Run all tests
npm run test:watch    # Watch mode
npm run test:coverage # With coverage report
```

## Questions?

Open an issue or start a discussion. We're happy to help!
