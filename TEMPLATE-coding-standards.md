# [PROJECT_NAME] Coding Standards

## Overview

This document outlines the coding standards, best practices, and conventions for the [PROJECT_NAME] project. These standards are based on industry best practices and are designed to ensure code quality, maintainability, and consistency across the codebase.

## [Primary Language] Style Guide

### General Standards
- Follow **[Style Guide Name]** strictly (e.g., PEP 8, Airbnb, Google Style Guide)
- Maximum line length: **[N] characters**
- Use **[single/double] quotes** for strings
- **Type hints/annotations are [mandatory/recommended]** for all function signatures
- Use **[Docstring Style]** for all modules, classes, and functions

### Code Formatting

#### Tools
```bash
# Required formatters and linters
[formatter-name]==[version]    # Code formatter
[import-sorter]==[version]     # Import sorting
[linter-name]==[version]       # Linter
[type-checker]==[version]      # Type checker
```

#### Configuration

```[config-format]
# [config-file-name]
[Configuration example showing:
- Line length
- Target version
- Include/exclude patterns
- Specific rules enabled/disabled]
```

### Type Hints/Annotations

```[language]
# Always use type hints/annotations
[Example showing:
- Function with typed parameters and return type
- Optional parameters
- Complex types (Dict, List, Union, etc.)
- Custom type definitions]
```

```[language]
# Use [validation library] for complex data structures
[Example showing:
- Data class/model with validation
- Field constraints
- Nested models
- Optional vs required fields]
```

### Docstrings/Documentation Comments

```[language]
"""[Module-level docstring example]

[Description of what the module does and its purpose]
"""

[Class docstring example with:
- Class description
- Attributes section
- Usage examples if complex]

[Function docstring example with:
- Brief description
- Args section with types and descriptions
- Returns section
- Raises section for exceptions
- Examples section if helpful]
```

### Import Organization

```[language]
# Import order:
# 1. Standard library imports
[Example]

# 2. Third-party imports
[Example]

# 3. Local application imports
[Example]

# 4. Relative imports (if used)
[Example]
```

### Naming Conventions

#### Variables
- **Local variables**: `[convention]` (e.g., snake_case, camelCase)
- **Constants**: `[convention]` (e.g., UPPER_SNAKE_CASE)
- **Private variables**: `[convention]` (e.g., _leading_underscore)

#### Functions/Methods
- **Public functions**: `[convention]` (e.g., snake_case, camelCase)
- **Private functions**: `[convention]` (e.g., _leading_underscore)
- **Boolean functions**: `[convention]` (e.g., is_valid, has_permission)

#### Classes
- **Class names**: `[convention]` (e.g., PascalCase)
- **Private classes**: `[convention]` (e.g., _LeadingUnderscore)
- **Abstract classes**: `[convention]` (e.g., AbstractBase)

#### Files/Modules
- **File names**: `[convention]` (e.g., snake_case.py, kebab-case.js)
- **Test files**: `[convention]` (e.g., test_module.py, module.test.js)

### Code Organization

```[language]
# Class structure order:
[Example showing:
1. Class docstring
2. Class-level constants
3. Class-level variables
4. __init__ / constructor
5. Public methods
6. Private methods
7. Static methods
8. Class methods
9. Properties]
```

### Error Handling

```[language]
# Always use specific exception types
[Example of proper error handling with:
- Specific exception catching
- Proper error messages
- Re-raising with context
- Cleanup in finally blocks
- Custom exception classes]
```

### Best Practices

#### General
- ✅ Write self-documenting code with clear variable/function names
- ✅ Keep functions small and focused (single responsibility principle)
- ✅ Use early returns to avoid deep nesting
- ✅ Prefer composition over inheritance
- ✅ Use descriptive variable names over comments when possible

#### [Language]-Specific
- ✅ [Practice 1 specific to the language]
- ✅ [Practice 2 specific to the language]
- ✅ [Practice 3 specific to the language]
- ✅ [Practice 4 specific to the language]
- ✅ [Practice 5 specific to the language]

## [Secondary Language] Style Guide

### General Standards
- Follow **[Style Guide]** for [framework] (e.g., Airbnb for React)
- **[Linter] + [Formatter]** for formatting
- **[Quote style]** for strings ([N] char line length)
- **[Component style]** (e.g., Functional components with hooks)
- **[API style]** (e.g., Composition API with TypeScript)

### Configuration

```[config-format]
# [config-file-name]
[Configuration example]
```

### Component Structure

```[language]
[Example of properly structured component with:
- Imports
- Type definitions
- Component definition
- Props interface/type
- State management
- Effects/lifecycle
- Helper functions
- Return/template]
```

### State Management

```[language]
[Example showing:
- State initialization
- State updates
- Derived state
- Global state access]
```

### Best Practices

- ✅ [Practice 1]
- ✅ [Practice 2]
- ✅ [Practice 3]
- ✅ [Practice 4]
- ✅ [Practice 5]

## Database & ORM Standards

### Model Definition

```[language]
[Example of database model with:
- Table name
- Primary key
- Foreign keys
- Indexes
- Constraints
- Relationships
- Timestamps]
```

### Queries

```[language]
# Always use parameterized queries
[Example of safe query]

# Avoid N+1 queries
[Example showing eager loading]

# Use proper indexing
[Example of efficient query]
```

### Migrations

```bash
# Generate migration
[Command to generate migration]

# Review migration before applying
[Command to review]

# Apply migration
[Command to apply]

# Rollback if needed
[Command to rollback]
```

## API Design Standards

### Endpoint Naming

- Use **[convention]** for endpoints (e.g., kebab-case, snake_case)
- Follow **[REST/GraphQL/RPC]** conventions
- Use proper HTTP methods: `GET`, `POST`, `PUT`, `PATCH`, `DELETE`

### Request/Response Format

```[language]
# Request
[Example request with:
- Headers
- Body structure
- Query parameters]

# Response
[Example response with:
- Status code
- Headers
- Body structure
- Error format]
```

### Error Responses

```[language]
# Standard error format
[Example showing:
- Error code
- Error message
- Error details
- Request ID
- Timestamp]
```

### Versioning

- API versioning: `[METHOD]` (e.g., URL path /v1/, header, query param)
- Breaking changes require new version
- Maintain backward compatibility for [N] versions

## Testing Standards

### Test Structure

```[language]
[Example test with:
- Test name
- Setup/arrange
- Action/act
- Assertion
- Cleanup]
```

### Test Naming

- Test functions: `test_[function_name]_[scenario]_[expected_result]`
- Test classes: `Test[ClassName]`
- Test files: `test_[module_name].[ext]` or `[module_name].test.[ext]`

### Test Coverage

- **Minimum overall coverage**: [X]%
- **Critical path coverage**: [Y]%
- **Test types**:
  - Unit tests: [Coverage target]
  - Integration tests: [Coverage target]
  - E2E tests: [Coverage target]

### Mocking & Fixtures

```[language]
[Example showing:
- How to create mocks
- How to use fixtures
- Proper cleanup]
```

### Best Practices

- ✅ Test behavior, not implementation
- ✅ One assertion per test (when possible)
- ✅ Use descriptive test names
- ✅ Arrange-Act-Assert pattern
- ✅ Test edge cases and error conditions
- ✅ Keep tests independent and isolated
- ✅ Avoid test interdependencies

## Git & Version Control Standards

### Branch Naming

```
[type]/[issue-number]-[brief-description]

Examples:
feature/123-add-user-authentication
fix/456-resolve-memory-leak
docs/update-api-documentation
refactor/789-simplify-data-processing
```

### Commit Messages

Follow [Conventional Commits](https://www.conventionalcommits.org/):

```
[type]([optional scope]): [description]

[optional body]

[optional footer]
```

**Types**:
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (no logic change)
- `refactor`: Code refactoring
- `test`: Adding or updating tests
- `chore`: Maintenance tasks
- `perf`: Performance improvements
- `ci`: CI/CD changes
- `build`: Build system changes

**Examples**:
```
feat(auth): add JWT token refresh mechanism
fix(api): resolve race condition in data fetching
docs(readme): update installation instructions
test(integration): add tests for payment flow
```

### Pull Request Guidelines

- ✅ Link to issue: `Closes #123` or `Fixes #456`
- ✅ Clear description of changes
- ✅ Include screenshots for UI changes
- ✅ Ensure all tests pass
- ✅ Update documentation
- ✅ Request review from appropriate team members
- ✅ Squash commits before merging
- ✅ Delete branch after merge

## Code Review Guidelines

### As a Reviewer

- ✅ Review within [N] hours/days
- ✅ Check for logic errors
- ✅ Verify test coverage
- ✅ Ensure coding standards are followed
- ✅ Look for potential security issues
- ✅ Suggest improvements constructively
- ✅ Approve only when fully satisfied

### Review Checklist

- [ ] Code follows project style guide
- [ ] All tests pass
- [ ] New code has tests
- [ ] Documentation is updated
- [ ] No sensitive data in code
- [ ] Error handling is appropriate
- [ ] Performance considerations addressed
- [ ] Security best practices followed

## Documentation Standards

### Code Comments

```[language]
# Use comments to explain WHY, not WHAT
[Example of good comment explaining reasoning]

# Avoid obvious comments
[Example of bad comment that states the obvious]
```

### README Files

Each module/package should have a README with:
- Purpose and overview
- Installation/setup instructions
- Usage examples
- API reference (if applicable)
- Configuration options
- Contributing guidelines

### API Documentation

- Use [tool] for API documentation (e.g., Swagger, JSDoc)
- Document all endpoints
- Include request/response examples
- Document error codes
- Keep documentation in sync with code

## Security Standards

### Input Validation

- ✅ Validate all user inputs
- ✅ Use allowlists over denylists
- ✅ Sanitize inputs before processing
- ✅ Use validation libraries ([library name])

### Authentication & Authorization

- ✅ Never store passwords in plain text
- ✅ Use [hashing algorithm] for passwords
- ✅ Implement proper session management
- ✅ Use HTTPS for all communications
- ✅ Implement rate limiting

### Data Protection

- ✅ Encrypt sensitive data at rest
- ✅ Use environment variables for secrets
- ✅ Never commit secrets to version control
- ✅ Implement proper access controls
- ✅ Log security events

### Dependencies

- ✅ Keep dependencies up to date
- ✅ Review dependency security advisories
- ✅ Use dependency scanning tools
- ✅ Pin dependency versions in production

## Performance Standards

### General Guidelines

- ✅ Optimize for readability first, then performance
- ✅ Profile before optimizing
- ✅ Cache expensive operations
- ✅ Use appropriate data structures
- ✅ Avoid premature optimization

### Database Performance

- ✅ Use proper indexes
- ✅ Avoid N+1 queries
- ✅ Use connection pooling
- ✅ Implement pagination for large datasets
- ✅ Use database query analysis tools

### API Performance

- ✅ Implement response caching
- ✅ Use pagination for list endpoints
- ✅ Implement rate limiting
- ✅ Optimize payload size
- ✅ Use compression

## Accessibility Standards (for UI/Frontend)

- ✅ Use semantic HTML
- ✅ Provide alt text for images
- ✅ Ensure keyboard navigation
- ✅ Maintain sufficient color contrast
- ✅ Support screen readers
- ✅ Follow [WCAG 2.1] Level [AA/AAA]

## CI/CD Standards

### Pre-commit Hooks

```bash
# Install pre-commit hooks
[command]

# Hooks to include:
- Code formatting
- Linting
- Type checking
- Unit tests (optional)
```

### CI Pipeline

Required checks before merge:
- [ ] All tests pass
- [ ] Code coverage meets threshold
- [ ] Linting passes
- [ ] Type checking passes
- [ ] Security scan passes
- [ ] Build succeeds

## Tools & Automation

### Required Development Tools

- **[Tool 1]**: [Purpose and installation]
- **[Tool 2]**: [Purpose and installation]
- **[Tool 3]**: [Purpose and installation]

### IDE Configuration

- Use [.editorconfig](../.editorconfig) for consistent formatting
- Recommended IDE settings:
  ```[format]
  [IDE-specific settings]
  ```

## Enforcement

- Pre-commit hooks enforce formatting and linting
- CI pipeline blocks PRs that don't meet standards
- Code review ensures adherence to best practices
- Regular team discussions to refine standards

## References

- [[Style Guide Name] Official Documentation]([URL])
- [[Framework] Best Practices]([URL])
- [Project-specific references]

---

**Document Version**: [VERSION]  
**Last Updated**: [DATE]  
**Maintained By**: [TEAM/PERSON]
