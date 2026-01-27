# Contributing to Sysponse

Thank you for contributing to Sysponse! This guide will help you understand our development workflow and standards.

---

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Branch Naming Conventions](#branch-naming-conventions)
- [Commit Message Standards](#commit-message-standards)
- [Pull Request Process](#pull-request-process)
- [Coding Standards](#coding-standards)
- [Testing Requirements](#testing-requirements)

---

## Code of Conduct

All team members must adhere to our [Code of Conduct](CODE_OF_CONDUCT.md). Please read it before contributing.

---

## Getting Started

1. **Clone the repository** you want to work on
2. **Set up your development environment** according to the repository's README
3. **Create a feature branch** following our naming conventions
4. **Make your changes** following our coding standards
5. **Test thoroughly** before submitting
6. **Submit a pull request** following our PR guidelines

---

## Development Workflow

We use **Feature Isolation** as our branching strategy:

1. All work happens in feature branches
2. Feature branches are created from `main` (or `develop` if applicable)
3. Features are merged back via Pull Request after review
4. `main` branch is always deployable

---

## Branch Naming Conventions

We follow **conventional branch naming** to keep our repository organized:

### Format
```
<type>/<short-description>
```

### Types
- **feature/** - New features or enhancements
  - Example: `feature/add-incident-search`
- **bugfix/** - Bug fixes for non-production issues
  - Example: `bugfix/fix-login-validation`
- **hotfix/** - Urgent fixes for production issues
  - Example: `hotfix/fix-critical-security-issue`
- **refactor/** - Code refactoring without functional changes
  - Example: `refactor/simplify-auth-logic`
- **docs/** - Documentation updates
  - Example: `docs/update-api-documentation`
- **test/** - Adding or updating tests
  - Example: `test/add-unit-tests-for-dispatch`
- **chore/** - Maintenance tasks (dependencies, tooling, etc.)
  - Example: `chore/update-dependencies`
- **release/** - Release preparation branches
  - Example: `release/v2.1.0`

### Guidelines
- Use lowercase
- Use hyphens to separate words
- Be descriptive but concise
- Avoid special characters

---

## Commit Message Standards

We use **Semantic Commit Messages** (Conventional Commits) to maintain clear project history:

### Format
```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types
- **feat**: New feature
- **fix**: Bug fix
- **docs**: Documentation changes
- **style**: Code style changes (formatting, missing semicolons, etc.)
- **refactor**: Code refactoring
- **perf**: Performance improvements
- **test**: Adding or updating tests
- **chore**: Maintenance tasks
- **ci**: CI/CD changes
- **build**: Build system changes

### Examples

```
feat(incident): add advanced search functionality

Implement advanced search for incidents with filters for date range,
status, and assigned resources.

Closes #123
```

```
fix(cad): resolve dispatch queue race condition

Fixed race condition when multiple dispatchers assign units simultaneously.
Added proper locking mechanism.

Fixes #456
```

```
chore(deps): update .NET SDK to 8.0.1
```

### Guidelines
- Use present tense ("add" not "added")
- Use imperative mood ("move" not "moves")
- First line should be 50 characters or less
- Include scope when applicable (module/component name)
- Reference issue numbers in footer

---

## Pull Request Process

### Before Submitting

1. ✅ Ensure your branch is up to date with the target branch
2. ✅ Run all tests locally and verify they pass
3. ✅ Run linters and fix any issues
4. ✅ Update documentation if needed
5. ✅ Add/update tests for your changes

### PR Title

Use the same format as commit messages:
```
<type>(<scope>): <description>
```

Example: `feat(mobile): add offline incident caching`

### PR Description

Use the pull request template provided. Include:
- **Summary**: What does this PR do?
- **Changes**: List of key changes
- **Testing**: How was this tested?
- **Screenshots**: If UI changes are involved
- **Related Issues**: Link to related issues

### Review Process

1. At least one team member must review and approve
2. All automated checks must pass
3. Resolve all review comments before merging
4. Squash commits if there are many small commits
5. Use "Squash and merge" or "Rebase and merge" as appropriate

---

## Coding Standards

### .NET/C#

- Follow [Microsoft C# Coding Conventions](https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions)
- Use meaningful variable and method names
- Keep methods small and focused
- Use async/await for I/O operations
- Handle exceptions appropriately
- Use dependency injection
- Follow SOLID principles

### TypeScript/JavaScript

- Use TypeScript for type safety
- Follow [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript)
- Use functional components and hooks in React
- Avoid `any` type in TypeScript
- Use ESLint and Prettier
- Write self-documenting code

### General Principles

- **DRY**: Don't Repeat Yourself
- **KISS**: Keep It Simple, Stupid
- **YAGNI**: You Aren't Gonna Need It
- Write code that is easy to read and maintain
- Comment only when necessary (code should be self-explanatory)
- Prioritize performance in critical paths

---

## Testing Requirements

### Unit Tests

- Write unit tests for all business logic
- Aim for >80% code coverage
- Use meaningful test names that describe what is being tested
- Follow AAA pattern: Arrange, Act, Assert

### Integration Tests

- Test integration points (APIs, databases, external services)
- Use test databases or mocks for external dependencies

### End-to-End Tests

- Test critical user workflows
- Ensure main features work as expected

### Test Naming

```csharp
// C# - xUnit
[Fact]
public void CreateIncident_WithValidData_ReturnsCreatedIncident()
{
    // Arrange
    // Act
    // Assert
}
```

```typescript
// TypeScript - Jest
describe('IncidentService', () => {
  it('should create incident with valid data', () => {
    // Arrange
    // Act
    // Assert
  });
});
```

---

## Technology-Specific Guidelines

### .NET Projects

- Target latest LTS version of .NET
- Use nullable reference types
- Follow repository pattern for data access
- Use AutoMapper for object mapping
- Implement proper logging with ILogger

### React/TypeScript Projects

- Use functional components with hooks
- Implement proper error boundaries
- Use React Query for data fetching
- Follow component composition patterns
- Implement proper accessibility (a11y)

### Blazor Projects

- Use component-based architecture
- Implement proper state management
- Use SignalR for real-time features
- Follow Blazor best practices

### Azure Functions

- Keep functions small and focused
- Use dependency injection
- Implement proper error handling
- Use durable functions for long-running processes

---

## Questions?

If you have questions or need help, check our [Support Resources](SUPPORT.md) or reach out to your team lead.

---

**Thank you for contributing to Sysponse! Together, we're building technology that saves lives.**
