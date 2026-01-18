# Testing

This project uses a validation-based testing approach.

## Running Tests

```bash
npm test
```

This runs:
1. **XO linting** - Code style and quality checks
2. **Validation tests** (`test.js`) - Validates user JSON files and theme CSS

## What's Tested

### User JSON Validation
- Files must have `.json` extension
- Filenames must be valid domain IDs
- JSON must be valid and parseable
- Must have `copyright` field (unless `locked`)
- No deprecated `version` field
- `gravatar` field must be boolean (not string)

### Theme CSS Validation
- CSS files must be valid and parseable

## Adding Tests

The main test file is `test.js` in the repository root. It uses Node.js built-in assertions and file system operations.

## CI/CD

Tests run automatically on:
- Push to `master`
- Pull requests targeting `master`

Tested on Node.js 20 and 22.
