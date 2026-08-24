---
name: rsshub-conventions
description: Development conventions and patterns for RSSHub. JavaScript Hono project with conventional commits.
---

# Rsshub Conventions

> Generated from [xiaomizhoubaobei/RSSHub](https://github.com/xiaomizhoubaobei/RSSHub) on 2026-08-24

## Overview

This skill teaches Claude the development patterns and conventions used in RSSHub.

## Tech Stack

- **Primary Language**: JavaScript
- **Framework**: Hono
- **Architecture**: hybrid module organization
- **Test Location**: mixed
- **Test Framework**: vitest

## When to Use This Skill

Activate this skill when:
- Making changes to this repository
- Adding new features following established patterns
- Writing tests that match project conventions
- Creating commits with proper message format

## Commit Conventions

Follow these commit message conventions based on 100 analyzed commits.

### Commit Style: Conventional Commits

### Prefixes Used

- `chore`
- `fix`
- `feat`
- `style`

### Message Guidelines

- Average message length: ~60 characters
- Keep first line concise and descriptive
- Use imperative mood ("Add feature" not "Added feature")


*Commit message example*

```text
chore: use mdast for route identification script
```

*Commit message example*

```text
fix(routes/miyuki): format news titles with bracketed categories and keep full-text body-only (#21377)
```

*Commit message example*

```text
style: auto format
```

*Commit message example*

```text
feat(routes/cognition): add category support to cognition blog route (#21394)
```

*Commit message example*

```text
test(header-generator): improve header validation (#21492)
```

*Commit message example*

```text
chore: fix deps not found in identify
```

*Commit message example*

```text
chore: fix PR number not found
```

*Commit message example*

```text
chore: wait for startup
```

## Architecture

### Project Structure: Single Package

This project uses **hybrid** module organization.

### Configuration Files

- `.github/workflows/build-assets.yml`
- `.github/workflows/codeql.yml`
- `.github/workflows/comment-on-issue.yml`
- `.github/workflows/dependabot-fork.yml`
- `.github/workflows/docker-release.yml`
- `.github/workflows/docker-test-cont.yml`
- `.github/workflows/docker-test.yml`
- `.github/workflows/format.yml`
- `.github/workflows/ghcr-retention.yml`
- `.github/workflows/issue-command.yml`
- `.github/workflows/lint.yml`
- `.github/workflows/npm-publish.yml`
- `.github/workflows/pr-review.yml`
- `.github/workflows/semgrep.yml`
- `.github/workflows/similar-issues.yml`
- `.github/workflows/stale.yml`
- `.github/workflows/test-full-routes.yml`
- `.github/workflows/test.yml`
- `.github/workflows/update-nix-hash.yml`
- `Dockerfile`
- `docker-compose.yml`
- `package.json`

### Guidelines

- This project uses a hybrid organization
- Follow existing patterns when adding new code

## Code Style

### Language: JavaScript

### Naming Conventions

| Element | Convention |
|---------|------------|
| Files | camelCase |
| Functions | camelCase |
| Classes | PascalCase |
| Constants | SCREAMING_SNAKE_CASE |

### Import Style: Path Aliases (@/, ~/)

### Export Style: Mixed Style


*Preferred import style*

```typescript
// Use path aliases for imports
import { Button } from '@/components/Button'
import { useAuth } from '@/hooks/useAuth'
import { api } from '@/lib/api'
```

## Testing

### Test Framework: vitest

### File Pattern: `*.test.ts`

### Test Types

- **Unit tests**: Test individual functions and components in isolation
- **Integration tests**: Test interactions between multiple components/services

### Mocking: msw

### Coverage

This project has coverage reporting configured. Aim for 80%+ coverage.


*Test file structure*

```typescript
import { describe, it, expect } from 'vitest'

describe('MyFunction', () => {
  it('should return expected result', () => {
    const result = myFunction(input)
    expect(result).toBe(expected)
  })
})
```

## Error Handling

### Error Handling Style: Try-Catch Blocks


*Standard error handling pattern*

```typescript
try {
  const result = await riskyOperation()
  return result
} catch (error) {
  console.error('Operation failed:', error)
  throw new Error('User-friendly message')
}
```

## Common Workflows

These workflows were detected from analyzing commit patterns.

### Feature Development

Standard feature implementation workflow

**Frequency**: ~5 times per month

**Steps**:
1. Add feature implementation
2. Add tests for feature
3. Update documentation

**Files typically involved**:
- `lib/routes/miyuki/*`
- `lib/routes/cognition/*`
- `lib/routes/apple/*`
- `**/*.test.*`
- `**/api/**`

**Example commit sequence**:
```
fix(routes/miyuki): format news titles with bracketed categories and keep full-text body-only (#21377)
style: auto format
chore: fix deps not found in identify
```


## Best Practices

Based on analysis of the codebase, follow these practices:

### Do

- Use conventional commit format (feat:, fix:, etc.)
- Write tests using vitest
- Follow *.test.ts naming pattern
- Use camelCase for file names
- Prefer mixed exports

### Don't

- Don't use long relative imports (use aliases)
- Don't write vague commit messages
- Don't skip tests for new features
- Don't deviate from established patterns without discussion

---

*This skill was auto-generated by [ECC Tools](https://ecc.tools). Review and customize as needed for your team.*
