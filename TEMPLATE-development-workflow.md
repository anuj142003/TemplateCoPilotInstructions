# [PROJECT_NAME] Development Workflow

## Overview

This document outlines the development workflow for the [PROJECT_NAME] project, from initial setup through feature delivery. We follow a [DEVELOPMENT_APPROACH] approach with [DEVELOPMENT_ENVIRONMENT] and [CI_CD_METHOD].

## Local Development Setup

### Prerequisites

- [Tool 1] [version]+ ([purpose])
- [Tool 2] [version]+
- [Tool 3] (recommended) or [Alternative]
- [Language] [version]+ (for [purpose])
- [Runtime] [version]+ (for [purpose])

### Initial Setup

```bash
# Clone the repository
git clone [REPOSITORY_URL]
cd [REPOSITORY_NAME]

# Copy environment template
cp .env.example .env

# Edit .env file with your credentials
# Required variables:
# - [VAR_1]
# - [VAR_2]
# - [VAR_3]
# - [VAR_4]

# Install pre-commit hooks
[command to install hooks]

# Build and start all services
make setup
# Or manually:
[manual setup commands]

# Verify all services are running
[verification command]

# Run database migrations (if applicable)
[migration command]

# Check logs
[log command]
```

### Environment Variables

All configuration is managed through `.env` files:

```bash
# .env.example - Template file (committed to repo)
# .env - Local configuration (never committed, in .gitignore)

# [Category 1] Configuration
[VAR_NAME]=[description and example]
[VAR_NAME]=[description and example]

# [Category 2] Configuration
[VAR_NAME]=[description and example]
[VAR_NAME]=[description and example]

# [Category 3] Configuration
[VAR_NAME]=[description and example]
[VAR_NAME]=[description and example]

# Application Configuration
LOG_LEVEL=[INFO/DEBUG/WARNING]
ENVIRONMENT=[development/staging/production]

# [Additional categories as needed]
```

### Makefile Commands

```makefile
# Makefile - Development shortcuts

.PHONY: setup build up down restart logs test lint format clean

# Initial setup
setup:
	@echo "Setting up [PROJECT_NAME] development environment..."
	[setup commands]

# Build all containers/compile code
build:
	[build command]

# Start all services
up:
	[start command]

# Stop all services
down:
	[stop command]

# Restart all services
restart:
	[restart command]

# View logs
logs:
	[log command]

# Run tests
test:
	[test commands]

# Run linters and formatters
lint:
	[lint commands]

# Format code
format:
	[format commands]

# Run type checker
typecheck:
	[typecheck command]

# Clean build artifacts
clean:
	[clean commands]

# Database operations
migrate:
	[migration command]

migrate-create:
	[create migration command]

migrate-rollback:
	[rollback command]
```

## Development Workflow

### 1. Planning & Issue Creation

Before starting work:

1. **Check for existing issues**: Search to avoid duplicates
2. **Create/assign issue**: Use appropriate issue template
3. **Add labels**: Assign priority, type, and component labels
4. **Link to project board**: Add to current sprint/milestone
5. **Discuss approach**: Comment on complex issues before starting

### Issue Templates

#### Feature Request
```markdown
## Description
[Clear description of the feature]

## User Story
As a [user type], I want [goal] so that [benefit]

## Acceptance Criteria
- [ ] [Criterion 1]
- [ ] [Criterion 2]
- [ ] [Criterion 3]

## Technical Notes
[Implementation considerations]

## Design Mockups
[If applicable]
```

#### Bug Report
```markdown
## Description
[Clear description of the bug]

## Steps to Reproduce
1. [Step 1]
2. [Step 2]
3. [Step 3]

## Expected Behavior
[What should happen]

## Actual Behavior
[What actually happens]

## Environment
- OS: [OS and version]
- Browser: [If applicable]
- Version: [Application version]

## Screenshots/Logs
[If applicable]
```

### 2. Branch Creation

```bash
# Ensure you're on the latest main/develop branch
git checkout [main/develop]
git pull origin [main/develop]

# Create feature branch
git checkout -b [type]/[issue-number]-[brief-description]

# Examples:
git checkout -b feature/123-add-user-dashboard
git checkout -b fix/456-memory-leak-in-cache
git checkout -b docs/update-api-documentation
```

### 3. Development Process

#### Feature Implementation

Follow this sequence for features:

1. **Design/Plan**
   - Review requirements
   - Design data models (if needed)
   - Plan API endpoints (if needed)
   - Sketch component structure (if applicable)

2. **Implement [Layer 1]** (e.g., Database/Models)
   ```bash
   # Create models
   [specific steps for your project]
   
   # Generate migration
   [migration command]
   
   # Apply migration
   [apply command]
   ```

3. **Implement [Layer 2]** (e.g., API/Business Logic)
   ```bash
   [specific steps for your project]
   ```

4. **Implement [Layer 3]** (e.g., Frontend/UI)
   ```bash
   [specific steps for your project]
   ```

5. **Testing**
   - Write unit tests
   - Write integration tests
   - Manual testing
   - Update test documentation

6. **Documentation**
   - Update API documentation
   - Update user documentation
   - Add code comments for complex logic
   - Update README if needed

#### Code Review Self-Checklist

Before requesting review:

- [ ] Code follows project coding standards
- [ ] All tests pass locally
- [ ] New tests added for new functionality
- [ ] Test coverage meets requirements
- [ ] No linting errors
- [ ] Type checking passes
- [ ] Documentation updated
- [ ] No debugging code or console.logs
- [ ] No commented-out code
- [ ] Environment variables documented
- [ ] Error handling implemented
- [ ] Security considerations addressed

### 4. Testing

```bash
# Run all tests
make test

# Run specific test suite
[command for specific suite]

# Run tests with coverage
[coverage command]

# View coverage report
[view coverage command]

# Run linter
make lint

# Run type checker
make typecheck

# Format code
make format
```

#### Test Types

**Unit Tests**
- Test individual functions/methods
- Mock external dependencies
- Fast execution
- Target: [X]% coverage

**Integration Tests**
- Test component interactions
- Use test database
- Mock external APIs
- Target: [Y]% coverage

**End-to-End Tests**
- Test complete user flows
- Use staging environment
- Real integrations
- Target: Critical paths only

### 5. Committing Changes

```bash
# Stage changes
git add [files]

# Commit with conventional commit format
git commit -m "[type]([scope]): [description]"

# Examples:
git commit -m "feat(auth): add password reset functionality"
git commit -m "fix(api): resolve race condition in user creation"
git commit -m "docs(readme): update installation instructions"
git commit -m "test(integration): add tests for payment flow"
git commit -m "refactor(database): optimize query performance"
```

**Commit Best Practices**:
- ✅ Write clear, descriptive messages
- ✅ Keep commits focused and atomic
- ✅ Reference issue numbers: `feat(api): add endpoint #123`
- ✅ Commit frequently during development
- ✅ Don't commit broken code
- ✅ Review changes before committing

### 6. Pull Request Process

#### Creating a Pull Request

```bash
# Push branch to remote
git push origin [branch-name]

# Create PR via GitHub UI or CLI
gh pr create --title "[Title]" --body "[Description]"
```

#### PR Title Format

```
[type]([scope]): [brief description]

Examples:
feat(dashboard): add real-time metrics display
fix(auth): resolve token expiration issue
docs(api): update authentication documentation
```

#### PR Description Template

```markdown
## Description
[Clear description of changes]

## Type of Change
- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] New feature (non-breaking change which adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] Documentation update
- [ ] Refactoring (no functional changes)
- [ ] Performance improvement
- [ ] Test updates

## Related Issues
Closes #[issue_number]
Related to #[issue_number]

## How Has This Been Tested?
[Description of testing approach]

- [ ] Unit tests
- [ ] Integration tests
- [ ] Manual testing
- [ ] E2E tests

## Screenshots (if applicable)
[Add screenshots for UI changes]

## Checklist
- [ ] My code follows the coding standards of this project
- [ ] I have performed a self-review of my code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings or errors
- [ ] I have added tests that prove my fix is effective or that my feature works
- [ ] New and existing unit tests pass locally with my changes
- [ ] Any dependent changes have been merged and published
- [ ] I have updated the changelog (if applicable)

## Additional Notes
[Any additional context]
```

### 7. Code Review

#### As an Author

- Respond to feedback promptly
- Address all comments
- Ask questions if feedback is unclear
- Request re-review after changes
- Be open to suggestions

#### As a Reviewer

- Review within [N] hours/days
- Be constructive and respectful
- Test changes locally if needed
- Check for:
  - Correctness
  - Code quality
  - Test coverage
  - Documentation
  - Security issues
  - Performance implications

#### Review Process

1. **Automated Checks**: CI/CD pipeline runs
2. **Peer Review**: At least [N] approval(s) required
3. **Address Feedback**: Author makes changes
4. **Final Approval**: Reviewer approves PR
5. **Merge**: Author or maintainer merges PR

### 8. Merging

```bash
# Ensure branch is up to date
git checkout [main/develop]
git pull origin [main/develop]
git checkout [feature-branch]
git merge [main/develop]

# Resolve any conflicts
# Test again after merge

# Push updates
git push origin [feature-branch]

# Merge via GitHub UI (preferred)
# Or via command line:
git checkout [main/develop]
git merge --squash [feature-branch]
git push origin [main/develop]

# Delete branch after merge
git branch -d [feature-branch]
git push origin --delete [feature-branch]
```

**Merge Strategy**: [Squash and merge / Merge commits / Rebase and merge]

## Continuous Integration

### CI Pipeline

On every push:
1. Install dependencies
2. Run linters
3. Run type checker
4. Run unit tests
5. Run integration tests
6. Check code coverage
7. Build application
8. Security scan

On PR:
- All CI checks must pass
- Required approvals met
- No merge conflicts
- Branch up to date with base

### CI Configuration

```yaml
[Example CI configuration file]
```

## Release Process

### Versioning

We follow [Semantic Versioning](https://semver.org/):
- **MAJOR**: Breaking changes
- **MINOR**: New features (backward compatible)
- **PATCH**: Bug fixes (backward compatible)

### Creating a Release

```bash
# Update version
[command to update version]

# Update changelog
[edit CHANGELOG.md]

# Commit version bump
git commit -m "chore: bump version to [X.Y.Z]"

# Create tag
git tag -a v[X.Y.Z] -m "Release v[X.Y.Z]"

# Push tag
git push origin v[X.Y.Z]

# Create release notes on GitHub
[via GitHub UI or CLI]
```

## Hotfix Process

For urgent production fixes:

```bash
# Create hotfix branch from main/production
git checkout -b hotfix/[issue-number]-[description] [main/production]

# Implement fix
# Test thoroughly
# Commit changes

# Create PR targeting main/production
# Fast-track review
# Merge and deploy

# Cherry-pick to develop if needed
git checkout develop
git cherry-pick [commit-hash]
```

## Common Tasks

### Adding a New Feature

1. Create issue
2. Create feature branch
3. Implement [end-to-end/layer by layer]
4. Write tests
5. Update documentation
6. Create PR
7. Code review
8. Merge

### Fixing a Bug

1. Reproduce bug
2. Create issue (if not exists)
3. Create fix branch
4. Write failing test
5. Implement fix
6. Verify test passes
7. Create PR
8. Code review
9. Merge

### Updating Dependencies

```bash
# Check for outdated dependencies
[command to check]

# Update specific dependency
[command to update]

# Test thoroughly after updates
make test

# Commit and create PR
git commit -m "chore(deps): update [dependency] to [version]"
```

## Troubleshooting

### Common Issues

**Issue**: [Common problem]
```bash
# Solution
[commands to resolve]
```

**Issue**: [Another common problem]
```bash
# Solution
[commands to resolve]
```

### Getting Help

1. Check documentation in `/docs`
2. Search closed issues
3. Ask in team chat/discussions
4. Contact [maintainer/team lead]

## Best Practices

- ✅ Keep branches small and focused
- ✅ Commit frequently with clear messages
- ✅ Write tests as you code
- ✅ Update documentation with code
- ✅ Review your own PR before requesting review
- ✅ Respond to PR feedback promptly
- ✅ Keep dependencies up to date
- ✅ Follow the coding standards
- ✅ Test locally before pushing
- ✅ Communicate blockers early

## References

- [Coding Standards](coding-standards.md)
- [Architecture Overview](architecture.md)
- [Testing Guide](../TESTING.md)
- [API Documentation](../api/)
- [Contributing Guidelines](../CONTRIBUTING.md)

---

**Document Version**: [VERSION]  
**Last Updated**: [DATE]  
**Maintained By**: [TEAM/PERSON]
