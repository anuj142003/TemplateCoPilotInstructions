# [PROJECT_NAME] - GitHub Copilot Development Instructions

## Project Context

**Project Name**: [PROJECT_NAME] - [PROJECT_TAGLINE]  
**Type**: [PROJECT_TYPE]  
**Tech Stack**: [LANGUAGES], [FRAMEWORKS], [DATABASES], [INFRASTRUCTURE]  
**AI Models**: [AI_SERVICES] (if applicable)

## Project Overview

[Provide 2-3 sentence overview of what the project does, its purpose, and key functionality]

[PROJECT_NAME] is designed to [PRIMARY_PURPOSE]. The system [KEY_FEATURES] and provides [PRIMARY_OUTPUTS].

## Architecture Summary

### [System Architecture / Component Structure]
- **[Component 1]**: [Brief description and responsibility]
- **[Component 2]**: [Brief description and responsibility]
- **[Component 3]**: [Brief description and responsibility]
- **[Component 4]**: [Brief description and responsibility]
- **[Component 5]**: [Brief description and responsibility]

### Key Technologies
- **Backend**: [Languages and versions], [Frameworks], [Key libraries]
- **Frontend**: [Frameworks], [State management], [UI libraries]
- **Database**: [Database type and version], [ORM], [Migration tool]
- **Infrastructure**: [Container platform], [Orchestration], [Deployment method]
- **Integrations**: [External services/APIs]

## Coding Standards

### [Primary Language] Style
- **Style Guide**: [e.g., PEP 8, Airbnb, Google Style Guide]
- **Formatter**: [e.g., Black, Prettier] ([line length])
- **Linter**: [e.g., ruff, ESLint]
- **Type Checking**: [e.g., mypy, TypeScript strict mode]
- **String Quotes**: [e.g., double quotes, single quotes]
- **Documentation**: [e.g., Google-style docstrings, JSDoc]

#### Required Tools
```[language]
[tool-name]==[version]    # [Purpose]
[tool-name]==[version]    # [Purpose]
[tool-name]==[version]    # [Purpose]
```

### [Secondary Language] Style (if applicable)
- **Style Guide**: [Reference]
- **Formatter**: [Tool and configuration]
- **Linter**: [Tool]
- **Component Style**: [e.g., functional components, class components]
- **Naming Conventions**: [Specific conventions]

### Testing Standards
- **Testing Framework**: [e.g., pytest, Jest, Mocha]
- **Test Timing**: Write tests [before/after] implementing features
- **Coverage Requirements**: Minimum [X]% overall, [Y]% for critical paths
- **Test Naming**: `test_<functionality>` or `describe/it` format
- **Test Location**: [e.g., tests/ directory, co-located __tests__]

### Git Workflow
- **Development Approach**: [e.g., Feature-driven, Trunk-based]
- **Branch Naming**: `[type]/[issue-number]-[description]`
  - Types: `feature`, `fix`, `docs`, `refactor`, `test`, `chore`
- **Commit Format**: [Conventional Commits](https://www.conventionalcommits.org/)
  - `[type]([scope]): [description]`
  - Types: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`
- **Merge Strategy**: [e.g., Squash and merge, Merge commits, Rebase]
- **Issue Linking**: Reference issues with `Closes #[NUMBER]` or `Fixes #[NUMBER]`

## Development Workflow

### Feature Development Process
1. Create GitHub issue using [template name] template
2. Create feature branch from `[main/develop]` branch
3. Implement feature **[end-to-end/incrementally]** ([specify layers if applicable])
4. Write tests **[before/after]** implementation
5. Update documentation **[during/after]** development
6. Create PR with completed checklist
7. Code review and address feedback
8. Merge after approval

### Key Principles
- Build features **[vertically/horizontally]** through [specify layers]
- Keep features **small and focused** ([X-Y days max])
- **[Database/Schema] migrations** are [auto-generated/manual] using [tool]
- All configuration via **[.env files/config files]** (never hardcode)
- **[Docker/Local/Cloud]-based** development

### Project-Specific Rules
- [Rule 1: e.g., "Always use dependency injection for services"]
- [Rule 2: e.g., "API responses must follow JSON:API spec"]
- [Rule 3: e.g., "All async operations must have timeout handlers"]
- [Rule 4: e.g., "Database queries must use parameterized statements"]
- [Rule 5: e.g., "All user inputs must be validated with Pydantic/Zod"]

## Copilot Usage Guidelines

### For [Primary Language] Code

When writing [language] code:

1. **Always include [type system features]**:
```[language]
[Example of properly typed function/class]
```

2. **Include comprehensive documentation**:
```[language]
[Example of properly documented function with docstring/JSDoc]
```

3. **Use [data validation library] for data structures**:
```[language]
[Example of data model with validation]
```

4. **Structured error handling**:
```[language]
[Example of proper error handling pattern]
```

### For [Secondary Language] Code

When writing [language] components:

1. **Use [component style] with [type system]**:
```[language]
[Example of properly typed component]
```

2. **Proper error handling and state management**:
```[language]
[Example of error handling in components]
```

### For [Special Component Type] (if applicable)

When creating or modifying [special components]:

1. **Follow [pattern name] pattern**:
```[language]
[Example of component pattern]
```

2. **Use [orchestration/framework] for [purpose]**:
```[language]
[Example of integration pattern]
```

### For Database Models

When creating database models:

1. **Use [ORM] with type hints**:
```[language]
[Example of database model]
```

2. **[Auto-generate/Manual] migrations**:
```bash
[Commands for generating/applying migrations]
```

### API Design

When creating API endpoints:

1. **Follow [RESTful/GraphQL/RPC] conventions**:
```[language]
[Example of properly structured endpoint]
```

2. **Use consistent response format**:
```[language]
[Example of response structure]
```

3. **Always include [authentication/validation/error handling]**:
```[language]
[Example of secured endpoint]
```

## Project Structure

```
[PROJECT_ROOT]/
├── [directory]/
│   ├── [subdirectory]/
│   │   └── [file patterns]
│   └── [purpose]
├── [directory]/
│   ├── [subdirectory]/
│   └── [purpose]
├── [directory]/
│   └── [purpose]
├── [config files]
└── [documentation]
```

### File Organization Rules
- [Rule 1: e.g., "Each module should have a single responsibility"]
- [Rule 2: e.g., "Test files mirror source file structure"]
- [Rule 3: e.g., "Shared utilities go in /shared or /common"]
- [Rule 4: e.g., "Feature folders contain all related files (component, styles, tests)"]

## Environment & Configuration

### Environment Variables
All configuration managed through `.env` files:
- `.env.example` - Template (committed to repo)
- `.env` - Local configuration (never committed, in .gitignore)

### Required Variables
```bash
# [Service/Component Name]
[VAR_NAME]=[description]
[VAR_NAME]=[description]

# [Another Service]
[VAR_NAME]=[description]
[VAR_NAME]=[description]
```

### Development Commands

```bash
# Setup
make setup              # Initial environment setup

# Development
make build             # Build containers/compile code
make up                # Start services
make down              # Stop services
make restart           # Restart services

# Testing
make test              # Run all tests
make test-[component]  # Run specific test suite
make coverage          # Generate coverage report

# Code Quality
make lint              # Run linters
make format            # Format code
make typecheck         # Run type checker

# Utilities
make logs              # View logs
make clean             # Clean build artifacts
make migrate           # Run database migrations
```

## Common Patterns

### [Pattern 1 Name]
```[language]
[Code example with explanation]
```

### [Pattern 2 Name]
```[language]
[Code example with explanation]
```

### [Pattern 3 Name]
```[language]
[Code example with explanation]
```

## Anti-Patterns to Avoid

### ❌ [Anti-pattern 1]
```[language]
# Don't do this:
[Bad example]
```

```[language]
# Do this instead:
[Good example]
```

### ❌ [Anti-pattern 2]
```[language]
# Don't do this:
[Bad example]
```

```[language]
# Do this instead:
[Good example]
```

## Debugging & Troubleshooting

### Common Issues

**Issue**: [Common problem description]
```bash
# Diagnostic command
[command to identify issue]

# Solution
[command to fix issue]
```

**Issue**: [Another common problem]
```bash
# Diagnostic command
[command to identify issue]

# Solution
[command to fix issue]
```

## Performance Considerations

- [Performance guideline 1]
- [Performance guideline 2]
- [Performance guideline 3]

## Security Guidelines

- [Security practice 1]
- [Security practice 2]
- [Security practice 3]
- [Security practice 4]

## Additional Resources

- [Project Overview](./TEMPLATE-project-overview.md)
- [Architecture Details](./TEMPLATE-architecture.md)
- [Coding Standards](./TEMPLATE-coding-standards.md)
- [Contributing Guide](./TEMPLATE-CONTRIBUTING.md)
- [Development Workflow](./TEMPLATE-development-workflow.md)
- [Deployment Guide](./TEMPLATE-deployment.md)
- [Usage Guide](./TEMPLATE-USAGE-GUIDE.md)

## Questions or Clarifications

For questions about these guidelines or project-specific decisions:
1. Check project documentation in `/docs`
2. Review closed issues and PRs for precedent
3. Ask in team discussions or standup
4. Contact [MAINTAINER_CONTACT]

---

**Last Updated**: [DATE]  
**Maintained By**: [TEAM/MAINTAINER_NAME]
