# 🤝 Contributing to ChatBot Builder Platform

Thank you for your interest in contributing to the ChatBot Builder Platform! This document provides guidelines and information to help you contribute effectively.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Branch Strategy](#branch-strategy)
- [Pull Request Process](#pull-request-process)
- [Coding Standards](#coding-standards)
- [Testing Guidelines](#testing-guidelines)
- [Documentation](#documentation)
- [Security](#security)

## 🤝 Code of Conduct

We are committed to providing a welcoming and inclusive environment for all contributors. Please be respectful and constructive in all interactions.

## 🚀 Getting Started

### Prerequisites

- **Node.js** 18+ and **Bun** 1.1.38+
- **Git** for version control
- **Neon PostgreSQL** database
- **Clerk** account for authentication
- **OpenAI** API key
- **Upstash Redis** for rate limiting

### Development Setup

1. **Fork and clone the repository:**
   ```bash
   git clone https://github.com/[your-username]/chatbot-builder-platform.git
   cd chatbot-builder-platform
   ```

2. **Install dependencies:**
   ```bash
   bun install
   ```

3. **Set up environment variables:**
   ```bash
   cp .env.example .env.local
   # Fill in your environment variables
   ```

4. **Set up the database:**
   ```bash
   bun run db:push
   bun run db:seed
   ```

5. **Start development server:**
   ```bash
   bun run dev
   ```

## 🔄 Development Workflow

### Branch Strategy

We use a **Git Flow** inspired branching strategy:

- **`main`** - Production-ready code only
- **`development`** - Integration branch for features
- **`staging`** - Pre-production testing
- **`feature/*`** - Individual features
- **`hotfix/*`** - Critical production fixes
- **`release/*`** - Release preparation

### Creating a Feature

1. **Create a feature branch:**
   ```bash
   git checkout development
   git pull origin development
   git checkout -b feature/your-feature-name
   ```

2. **Make your changes following our coding standards**

3. **Test your changes:**
   ```bash
   bun run lint
   bun run type-check
   bun run test
   bun run build
   ```

4. **Commit your changes:**
   ```bash
   git add .
   git commit -m "feat: add your feature description"
   ```

5. **Push and create a pull request:**
   ```bash
   git push origin feature/your-feature-name
   ```

## 🔀 Pull Request Process

### Before Creating a PR

- [ ] Code follows our style guidelines
- [ ] All tests pass
- [ ] Documentation is updated
- [ ] Security considerations are addressed
- [ ] Performance impact is minimal

### PR Requirements

1. **Descriptive title and summary**
2. **Link to related issue(s)**
3. **Type of change clearly identified**
4. **Test plan included**
5. **Screenshots for UI changes**
6. **Breaking changes documented**

### Review Process

- PRs require at least **1 approval** from maintainers
- All CI checks must pass
- Conflicts must be resolved
- Branch must be up-to-date with target

## 🎯 Coding Standards

### TypeScript/JavaScript

- Use **TypeScript** for all new code
- Follow **ESLint** and **Prettier** configurations
- Use **async/await** over Promises
- Prefer **const** over **let**
- Use **descriptive variable names**

### React/Next.js

- Use **functional components** with hooks
- Implement **proper error boundaries**
- Follow **Next.js best practices**
- Use **server components** when possible
- Implement **proper loading states**

### Database

- Use **Drizzle ORM** for database operations
- Write **migrations** for schema changes
- Include **proper indexes**
- Use **transactions** for complex operations

### API Design

- Follow **RESTful** conventions
- Use **proper HTTP status codes**
- Implement **input validation**
- Include **comprehensive error handling**
- Add **rate limiting** where appropriate

## 🧪 Testing Guidelines

### Unit Tests

- Write tests for **all business logic**
- Use **Jest** and **React Testing Library**
- Aim for **80%+ code coverage**
- Mock external dependencies

### Integration Tests

- Test **API endpoints**
- Test **database operations**
- Test **authentication flows**

### E2E Tests

- Test **critical user journeys**
- Use **Playwright** or **Cypress**
- Run tests in **CI/CD pipeline**

### Testing Commands

```bash
# Run all tests
bun run test

# Run tests in watch mode
bun run test:watch

# Run tests with coverage
bun run test:coverage

# Run E2E tests
bun run test:e2e
```

## 📚 Documentation

### Code Documentation

- Add **JSDoc comments** for functions
- Document **complex logic**
- Include **usage examples**
- Keep documentation **up-to-date**

### API Documentation

- Document all **API endpoints**
- Include **request/response examples**
- Document **error responses**
- Update **OpenAPI specifications**

## 🔒 Security

### Security Guidelines

- **Never commit secrets** or API keys
- **Sanitize user inputs**
- **Use parameterized queries**
- **Implement proper authentication**
- **Follow OWASP guidelines**

### Security Review

- All PRs undergo **security review**
- **Dependencies** are regularly audited
- **SAST tools** are integrated in CI
- **Security issues** are addressed promptly

## 🏷️ Commit Convention

We follow **Conventional Commits**:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

### Types

- **feat**: New feature
- **fix**: Bug fix
- **docs**: Documentation only changes
- **style**: Changes that don't affect code meaning
- **refactor**: Code change that neither fixes bug nor adds feature
- **perf**: Performance improvement
- **test**: Adding missing tests
- **chore**: Changes to build process or auxiliary tools

### Examples

```bash
feat(widget): add new customization options
fix(auth): resolve login redirect issue
docs(api): update authentication guide
```

## 🛠️ Tools and Scripts

### Available Scripts

```bash
# Development
bun run dev              # Start development server
bun run build            # Build for production
bun run start            # Start production server

# Code Quality
bun run lint             # Run ESLint
bun run lint:fix         # Fix ESLint issues
bun run type-check       # TypeScript type checking
bun run format           # Format code with Prettier

# Database
bun run db:push          # Push schema changes
bun run db:studio        # Open database studio
bun run db:seed          # Seed database

# Testing
bun run test             # Run tests
bun run test:coverage    # Run tests with coverage
```

## 🐛 Reporting Issues

### Bug Reports

When reporting bugs, please include:

- **Clear description** of the issue
- **Steps to reproduce**
- **Expected vs actual behavior**
- **Environment details**
- **Screenshots** if applicable

### Feature Requests

When requesting features, please include:

- **Problem description**
- **Proposed solution**
- **Use case scenarios**
- **Acceptance criteria**

## 💬 Getting Help

- **Issues**: For bug reports and feature requests
- **Discussions**: For questions and community chat
- **Email**: For security issues (security@example.com)

## 🎉 Recognition

Contributors will be recognized in:

- **README.md** contributors section
- **CHANGELOG.md** for significant contributions
- **GitHub Discussions** for community contributions

---

Thank you for contributing to the ChatBot Builder Platform! 🚀