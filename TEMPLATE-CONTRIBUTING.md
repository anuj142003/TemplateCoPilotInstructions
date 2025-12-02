# Contributing to [PROJECT_NAME]

Thank you for your interest in contributing to [PROJECT_NAME]! We welcome contributions from the community and appreciate your help in making this project better. Please follow the guidelines below to ensure a smooth contribution process.

## Code of Conduct

Please adhere to our Code of Conduct while contributing to this project. Be respectful and considerate to others in the community.

## How to Contribute

### 1. Fork the Repository

Start by forking the repository to your own GitHub account.

### 2. Clone Your Fork

Clone your forked repository to your local machine:

```bash
git clone https://github.com/[YOUR_USERNAME]/[REPO_NAME].git
cd [REPO_NAME]
```

### 3. Set Up Development Environment

Follow the setup instructions in the main [README.md](README.md#development) to configure your local development environment.

```bash
# Copy environment template
cp .env.example .env
# Edit .env with your credentials

# Install dependencies and start services
make setup

# Verify everything is working
make test
```

### 4. Create a Branch

Create a new branch for your feature or bug fix using the naming convention:

```bash
# For features
git checkout -b feature/[ISSUE_NUMBER]-[brief-description]

# For bug fixes
git checkout -b fix/[ISSUE_NUMBER]-[brief-description]

# For documentation
git checkout -b docs/[brief-description]
```

### 5. Make Changes

- Make your changes in the codebase
- Follow the coding standards outlined in [`docs/coding-standards.md`](docs/coding-standards.md)
- Write clear, self-documenting code with appropriate comments
- Add or update tests as needed
- Update documentation if you're changing functionality

### 6. Test Your Changes

Run tests to ensure that your changes do not break any existing functionality:

```bash
# Run all tests
make test

# Run specific test suite
make test-[component]

# Check code formatting
make lint

# Format code automatically
make format
```

Refer to [`docs/development-workflow.md`](docs/development-workflow.md) for detailed testing procedures.

### 7. Commit Your Changes

Commit your changes with a clear and descriptive commit message following [Conventional Commits](https://www.conventionalcommits.org/) format:

```bash
# Format: <type>(<scope>): <description>

# Examples:
git commit -m "feat(api): add endpoint for user preferences"
git commit -m "fix(auth): resolve token expiration issue"
git commit -m "docs(readme): update installation instructions"
git commit -m "test(integration): add tests for data collection"
git commit -m "refactor(agent): simplify data processing logic"
```

**Commit Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, no logic change)
- `refactor`: Code refactoring
- `test`: Adding or updating tests
- `chore`: Maintenance tasks, dependency updates
- `perf`: Performance improvements

### 8. Push to Your Fork

Push your changes to your forked repository:

```bash
git push origin [BRANCH_NAME]
```

### 9. Submit a Pull Request

1. Go to the original repository on GitHub
2. Click "New Pull Request"
3. Select your fork and branch
4. Fill out the pull request template with:
   - **Title**: Clear, descriptive title
   - **Description**: Detailed explanation of changes
   - **Issue Reference**: Link to related issue(s) using `Closes #[ISSUE_NUMBER]` or `Fixes #[ISSUE_NUMBER]`
   - **Testing**: How you tested the changes
   - **Screenshots**: If applicable (UI changes)
   - **Checklist**: Complete the PR checklist

### 10. Code Review Process

- A maintainer will review your pull request
- Address any feedback or requested changes
- Once approved, your PR will be merged

## Pull Request Guidelines

### Before Submitting

- ✅ Code follows project coding standards
- ✅ All tests pass locally
- ✅ New tests added for new functionality
- ✅ Documentation updated (if applicable)
- ✅ Commit messages follow conventional format
- ✅ Branch is up to date with main branch
- ✅ No merge conflicts

### PR Checklist Template

```markdown
## Description
[Describe your changes]

## Type of Change
- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] New feature (non-breaking change which adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] Documentation update
- [ ] Refactoring (no functional changes)

## Related Issues
Closes #[ISSUE_NUMBER]

## How Has This Been Tested?
[Describe testing process]

## Screenshots (if applicable)
[Add screenshots]

## Checklist
- [ ] My code follows the coding standards of this project
- [ ] I have performed a self-review of my code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings or errors
- [ ] I have added tests that prove my fix is effective or that my feature works
- [ ] New and existing unit tests pass locally with my changes
- [ ] Any dependent changes have been merged and published
```

## Reporting Issues

If you encounter bugs, have feature requests, or find documentation gaps:

1. **Search Existing Issues**: Check if the issue already exists
2. **Create New Issue**: If not found, create a new issue with:
   - Clear, descriptive title
   - Detailed description
   - Steps to reproduce (for bugs)
   - Expected vs actual behavior
   - Environment details (OS, versions, etc.)
   - Screenshots or logs (if applicable)

## Development Guidelines

### Coding Standards

- Follow language-specific style guides (see [`docs/coding-standards.md`](docs/coding-standards.md))
- Write self-documenting code with clear variable/function names
- Add comments for complex logic
- Use type hints (for Python) or TypeScript
- Keep functions small and focused (single responsibility)

### Testing Standards

- Write tests for all new features
- Maintain minimum [X]% code coverage
- Follow testing guidelines in [`docs/development-workflow.md`](docs/development-workflow.md)
- Test both happy paths and edge cases

### Documentation Standards

- Update README if adding new features
- Document API changes in relevant docs
- Add inline code comments for complex logic
- Update architecture docs for structural changes

## Communication

- **GitHub Issues**: For bug reports and feature requests
- **Pull Requests**: For code discussions
- **Discussions**: For general questions and ideas
- **Email**: [CONTACT_EMAIL] for security issues

## Recognition

Contributors are recognized in:
- GitHub contributors page
- Release notes (for significant contributions)
- Project documentation (for major features)

## Questions?

If you have questions about contributing, please:
1. Check existing documentation
2. Search closed issues for similar questions
3. Open a discussion on GitHub
4. Contact maintainers at [CONTACT_EMAIL]

Thank you for contributing to [PROJECT_NAME]! 🎉
