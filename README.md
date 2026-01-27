# .github Repository

This is the special `.github` repository for the **Sysponse** organization. Files in this repository provide default community health files, templates, and workflows that apply to all repositories in the organization.

---

## 📂 What's Inside

### Community Health Files

These files are automatically used by all repositories in the Sysponse organization (unless a repository has its own version):

- **[CONTRIBUTING.md](CONTRIBUTING.md)** - Development standards, branch naming conventions, commit message guidelines, and PR process
- **[CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)** - Team standards and expected professional behavior
- **[SECURITY.md](SECURITY.md)** - Security policy and vulnerability reporting procedures
- **[SUPPORT.md](SUPPORT.md)** - How to get help and support resources

### Organization Profile

- **[profile/README.md](profile/README.md)** - Organization profile that appears on the main GitHub organization page

### Issue Templates

Located in `ISSUE_TEMPLATE/`:

- **bug_report.md** - Template for reporting bugs
- **feature_request.md** - Template for suggesting new features
- **task.md** - Template for maintenance tasks and chores
- **question.md** - Template for asking questions
- **config.yml** - Configuration for issue template chooser

### Pull Request Template

- **[pull_request_template.md](pull_request_template.md)** - Standard PR template with comprehensive checklist for semantic commits, testing, security, and more

### Workflow Templates

Located in `workflow-templates/`:

Reusable GitHub Actions workflows that can be used across all repositories:

- **dotnet-build-test.yml** - .NET/C# build, test, and security scan
- **react-build-test.yml** - React/TypeScript build, test, lint, and bundle analysis
- **azure-functions-deploy.yml** - Azure Functions deployment pipeline
- **blazor-wasm-deploy.yml** - Blazor WebAssembly build and deployment to Azure Static Web Apps

Each workflow has an accompanying `.properties.json` file that defines metadata for the template.

### Dependabot Configuration

- **[dependabot.yml](dependabot.yml)** - Automated dependency updates for NuGet, npm, GitHub Actions, and Docker

---

## 🎯 Purpose

This repository serves as the central configuration hub for the Sysponse GitHub organization, ensuring:

- **Consistency**: All repositories follow the same standards and guidelines
- **Efficiency**: Templates and workflows can be reused across projects
- **Quality**: Comprehensive checklists and automated checks maintain code quality
- **Security**: Centralized security policies and automated dependency updates
- **Onboarding**: New team members have clear guidelines and resources

---

## 🚀 How to Use

### For Repository Maintainers

1. **Community Health Files**: These are automatically inherited by all repositories
2. **Issue Templates**: Automatically available in all repositories
3. **PR Template**: Automatically used when creating pull requests
4. **Workflow Templates**: Available in the "Actions" tab → "New workflow" in any repository

### Creating a New Repository

When you create a new repository in the Sysponse organization:

1. ✅ Community health files are automatically available
2. ✅ Issue and PR templates are ready to use
3. ✅ Add workflows from templates in the Actions tab
4. ✅ Dependabot is configured automatically

### Customizing for Specific Repositories

If a repository needs different guidelines:

1. Create repository-specific files with the same names
2. Repository-level files override organization-level defaults
3. Consider if changes should be applied organization-wide

---

## 📋 Development Standards

All Sysponse repositories follow these standards:

### Branch Naming
```
<type>/<description>
```
Types: `feature/`, `bugfix/`, `hotfix/`, `refactor/`, `docs/`, `test/`, `chore/`, `release/`

### Commit Messages
```
<type>(<scope>): <subject>
```
Types: `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `chore`, `ci`, `build`

### Technology Stack

- **Backend**: .NET/C#, ASP.NET Core, gRPC, Azure Functions
- **Frontend**: React, TypeScript, Blazor WebAssembly
- **Mobile**: .NET MAUI
- **Databases**: SQL Server, PostgreSQL, MongoDB, SQLite
- **Cloud**: Microsoft Azure

---

## 🔄 Updates

This repository is maintained by the Sysponse development team. Updates to community health files, templates, and workflows are reviewed and approved before being applied organization-wide.

### Proposing Changes

To suggest changes to organization-wide standards:

1. Create a branch in this repository
2. Make your changes
3. Submit a pull request with clear rationale
4. Changes will be reviewed by team leads
5. Once approved, changes apply to all repositories

---

## 📚 Resources

### Internal Documentation
- See [CONTRIBUTING.md](CONTRIBUTING.md) for full development guidelines
- See [SECURITY.md](SECURITY.md) for security best practices
- See [SUPPORT.md](SUPPORT.md) for getting help

### External Resources
- [GitHub Community Health Files](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)
- [GitHub Actions Workflow Templates](https://docs.github.com/en/actions/using-workflows/creating-starter-workflows-for-your-organization)
- [Dependabot Configuration](https://docs.github.com/en/code-security/dependabot/dependabot-version-updates/configuration-options-for-the-dependabot.yml-file)

---

## 🤝 About Sysponse

Sysponse is a Salem, Oregon-based company that develops emergency management software for first responders and public safety agencies. Our products include:

- Incident Management Systems
- CAD (Computer-Aided Dispatch) Systems
- Mobile Applications for Responding Resources
- Resource Tracking Solutions

**Our mission**: Build reliable, life-saving technology that first responders can depend on.

---

## 📞 Contact

For questions about this repository or organization standards:
- Team Leads
- Internal development channels
- See [SUPPORT.md](SUPPORT.md) for more contact options

---

**Building the future of emergency response, one commit at a time.** 🚨
