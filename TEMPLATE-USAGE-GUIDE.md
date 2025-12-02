# Copilot Instructions Template Guide

This folder contains standardized templates for setting up GitHub Copilot instructions for any project. These templates ensure consistency, completeness, and ease of setup across different projects.

## Templates Included

### Core Templates

1. **TEMPLATE-README.md**
   - Main project README structure
   - Overview, features, quick start
   - Architecture summary and documentation links

2. **TEMPLATE-CONTRIBUTING.md**
   - Contribution guidelines
   - Development setup
   - Pull request process
   - Code review guidelines

3. **.github/TEMPLATE-copilot-instructions.md**
   - GitHub Copilot-specific development instructions
   - Coding standards for AI assistance
   - Common patterns and anti-patterns
   - Project-specific guidelines for code generation

### Documentation Templates

4. **docs/TEMPLATE-project-overview.md**
   - Detailed project purpose and goals
   - Target users and problems solved
   - System architecture overview
   - Scope and success metrics

5. **docs/TEMPLATE-architecture.md**
   - Comprehensive technical architecture
   - Technology stack details
   - Component descriptions
   - Data flow and deployment architecture

6. **docs/TEMPLATE-coding-standards.md**
   - Language-specific style guides
   - Formatting and linting rules
   - Testing standards
   - Security and performance guidelines

7. **docs/TEMPLATE-development-workflow.md**
   - Development environment setup
   - Feature development process
   - Git workflow and branching strategy
   - CI/CD and release process

8. **docs/TEMPLATE-deployment.md**
   - Installation instructions
   - Configuration management
   - Service management
   - Monitoring, backup, and troubleshooting

## How to Use These Templates

### For New Projects

1. **Copy Templates to Your Project**
   ```bash
   # Create copilot instructions directory
   mkdir -p your-project/copilot-instructions/.github/docs
   
   # Copy templates
   cp TEMPLATE-README.md your-project/copilot-instructions/README.md
   cp TEMPLATE-CONTRIBUTING.md your-project/copilot-instructions/CONTRIBUTING.md
   cp .github/TEMPLATE-copilot-instructions.md your-project/copilot-instructions/.github/copilot-instructions.md
   cp docs/TEMPLATE-*.md your-project/copilot-instructions/docs/
   
   # Remove TEMPLATE- prefix
   cd your-project/copilot-instructions/docs/
   for file in TEMPLATE-*.md; do mv "$file" "${file#TEMPLATE-}"; done
   ```

2. **Fill in Project-Specific Information**
   
   Search for and replace all placeholder text in brackets:
   - `[PROJECT_NAME]` → Your project name
   - `[PROJECT_TAGLINE]` → Brief project description
   - `[PROJECT_TYPE]` → Type of project (e.g., "Multi-Agent AI Platform")
   - `[PRIMARY_PURPOSE]` → Main purpose statement
   - `[LANGUAGE]` → Programming language(s)
   - `[FRAMEWORK]` → Framework(s) used
   - And all other `[PLACEHOLDER]` text

3. **Customize for Your Needs**
   - Remove sections that don't apply
   - Add project-specific sections
   - Adjust examples to match your tech stack
   - Update configuration examples

4. **Link to GitHub Copilot**
   - Place `.github/copilot-instructions.md` in your project's `.github/` directory
   - GitHub Copilot will automatically discover and use it

### For Existing Projects

1. **Audit Current Documentation**
   - Review what documentation already exists
   - Identify gaps using templates as a checklist

2. **Merge Existing Content**
   - Copy relevant sections from existing docs
   - Fill in missing sections using templates
   - Maintain your project's voice and style

3. **Standardize Structure**
   - Reorganize existing docs to match template structure
   - Use consistent formatting and sections
   - Link documents together

4. **Validate Completeness**
   - Ensure all placeholders are filled
   - Verify all examples are project-specific
   - Test that Copilot can understand the instructions

## Placeholder Reference

### Common Placeholders

| Placeholder | Description | Example |
|------------|-------------|---------|
| `[PROJECT_NAME]` | Project name | "TaskMaster", "DataFlow" |
| `[PROJECT_TAGLINE]` | Brief description | "Task Management for Teams" |
| `[PROJECT_TYPE]` | Project category | "Web Application", "API Service" |
| `[VERSION_NUMBER]` | Current version | "1.0.0", "0.5.0-beta" |
| `[ORG]` | GitHub organization | "mycompany", "opensource-project" |
| `[REPO]` | Repository name | "taskmaster", "dataflow-api" |

### Technical Placeholders

| Placeholder | Description | Example |
|------------|-------------|---------|
| `[LANGUAGE]` | Programming language | "Python 3.11", "TypeScript" |
| `[FRAMEWORK]` | Framework used | "FastAPI", "React", "Vue.js" |
| `[DATABASE]` | Database system | "PostgreSQL 15", "MongoDB" |
| `[ARCHITECTURE_PATTERN]` | Architecture type | "Microservices", "Monolith" |
| `[DEPLOYMENT_METHOD]` | Deployment approach | "Docker Compose", "Kubernetes" |

### Configuration Placeholders

| Placeholder | Description | Example |
|------------|-------------|---------|
| `[VAR_NAME]` | Environment variable | "DATABASE_URL", "API_KEY" |
| `[URL]` | Application URL | "http://localhost:3000" |
| `[PORT]` | Port number | "8080", "5432" |
| `[PATH]` | File/directory path | "/opt/myapp", "C:\myapp" |

### Contact Placeholders

| Placeholder | Description | Example |
|------------|-------------|---------|
| `[TEAM/PERSON]` | Maintainer name | "DevOps Team", "John Smith" |
| `[CONTACT_EMAIL]` | Support email | "support@company.com" |
| `[MAINTAINER_CONTACT]` | Contact info | "@john-smith", "team@company.com" |

## Template Customization Guidelines

### Do's ✅

- **Do** fill in ALL placeholders with project-specific information
- **Do** remove sections that don't apply to your project
- **Do** add project-specific sections and examples
- **Do** keep documentation up to date as project evolves
- **Do** use consistent terminology across all documents
- **Do** provide real, working examples
- **Do** include actual commands that work in your environment

### Don'ts ❌

- **Don't** leave placeholder text in final documentation
- **Don't** include outdated or incorrect information
- **Don't** copy examples from other projects without adapting them
- **Don't** make documentation too generic
- **Don't** forget to update examples when technology changes
- **Don't** skip sections just because they seem optional

## Validation Checklist

Before finalizing your copilot instructions:

- [ ] All `[PLACEHOLDER]` text has been replaced
- [ ] All commands and code examples are tested and working
- [ ] Configuration examples match your actual configuration
- [ ] URLs and paths are correct for your project
- [ ] Contact information is accurate
- [ ] Version numbers are current
- [ ] Examples are project-specific, not generic
- [ ] Architecture diagrams reflect actual architecture
- [ ] Dependencies and prerequisites are complete
- [ ] All links work and point to correct locations
- [ ] Terminology is consistent across all documents
- [ ] Code examples follow your coding standards

## Template Structure Philosophy

### Consistency
All templates follow a consistent structure:
1. Title and overview
2. Core content organized by logical sections
3. Examples and code snippets
4. References and additional resources
5. Document metadata (version, date, maintainer)

### Completeness
Templates cover all essential aspects:
- **What**: Description and purpose
- **Why**: Rationale and benefits
- **How**: Step-by-step instructions
- **When**: Timing and workflow
- **Who**: Roles and responsibilities

### Clarity
Templates prioritize:
- Clear, actionable language
- Concrete examples over abstract descriptions
- Logical organization and flow
- Easy-to-scan formatting with headers, lists, and tables

## Maintaining Templates

### For Template Maintainers

- Review templates quarterly for relevance
- Update based on community feedback
- Add new placeholders as needs arise
- Improve examples and clarity
- Keep aligned with industry best practices

### For Template Users

- Report issues or suggest improvements
- Share your customized versions as inspiration
- Contribute back generalizable improvements
- Document any common customization patterns

## Examples of Well-Filled Templates

See the original Lighthouse project files in the parent directory for examples of these templates in use:
- `README.md`
- `CONTRIBUTING.md`
- `.github/copilot-instructions.md`
- `docs/project-overview.md`
- `docs/architecture.md`
- `docs/coding-standards.md`
- `docs/development-workflow.md`
- `docs/deployment.md`

## Quick Start Summary

1. **Copy** templates to your project
2. **Search and replace** all `[PLACEHOLDER]` text
3. **Customize** sections for your specific needs
4. **Validate** using the checklist above
5. **Place** `.github/copilot-instructions.md` in your project's `.github/` folder
6. **Test** with GitHub Copilot to ensure it works

## Support

For questions or issues with these templates:
- Review the original Lighthouse project as reference
- Check the validation checklist
- Ensure all placeholders are replaced
- Verify examples match your project

---

**Template Version**: 1.0.0  
**Last Updated**: December 2, 2025  
**Compatible With**: GitHub Copilot
