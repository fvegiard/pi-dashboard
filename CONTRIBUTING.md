# Contributing to pi-dashboard

Thank you for considering contributing to pi-dashboard! We welcome contributions from the community.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Setup](#development-setup)
- [Making Changes](#making-changes)
- [Submitting Changes](#submitting-changes)
- [Style Guide](#style-guide)
- [Testing](#testing)

## Code of Conduct

This project is committed to providing a welcoming and inspiring community for all. Please read and abide by our [Code of Conduct](./CODE_OF_CONDUCT.md).

## Getting Started

### Prerequisites
- Node.js 14.x or higher
- npm or yarn
- Git
- Basic familiarity with Electron and React/Vue development

### Fork and Clone
1. Fork the repository on GitHub
2. Clone your fork: `git clone https://github.com/YOUR_USERNAME/pi-dashboard.git`
3. Add upstream remote: `git remote add upstream https://github.com/fvegi/pi-dashboard.git`

## Development Setup

1. **Install Dependencies**
   ```bash
   cd pi-dashboard
   npm install
   ```

2. **Development Mode**
   ```bash
   npm run dev
   ```
   Starts the application with hot reload enabled.

3. **Build for Production**
   ```bash
   npm run build
   ```

4. **Run Tests**
   ```bash
   npm test
   ```

5. **Lint Code**
   ```bash
   npm run lint
   npm run lint:fix  # Auto-fix issues
   ```

## Making Changes

### Create a Feature Branch
```bash
git checkout -b feature/your-feature-name
```

Use descriptive branch names:
- `feature/add-new-dashboard-widget`
- `fix/incorrect-memory-calculation`
- `docs/update-readme`
- `test/add-unit-tests`

### Commit Guidelines

Follow [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types**:
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style (formatting, semicolons, etc.)
- `refactor`: Code refactoring
- `perf`: Performance improvements
- `test`: Adding or updating tests
- `chore`: Dependency updates, build tool changes

**Example**:
```
feat(dashboard): add real-time CPU usage widget

- Implement CPU monitoring using system APIs
- Add refresh interval configuration
- Display as animated gauge chart

Closes #123
```

## Submitting Changes

### Before Submitting
- [ ] Code builds successfully: `npm run build`
- [ ] Tests pass: `npm test`
- [ ] Linting passes: `npm run lint`
- [ ] Changes are well-documented
- [ ] Commits follow [Conventional Commits](#commit-guidelines)

### Create a Pull Request

1. **Rebase on Latest**
   ```bash
   git fetch upstream
   git rebase upstream/main
   ```

2. **Push to Your Fork**
   ```bash
   git push origin feature/your-feature-name
   ```

3. **Create Pull Request**
   - Go to GitHub repository
   - Click "New Pull Request"
   - Select your branch
   - Fill out the PR template
   - Describe what you changed and why

### PR Title Format
Follow [Conventional Commits](https://www.conventionalcommits.org/):
- `feat: add widget gallery page`
- `fix: resolve memory leak in data stream`
- `docs: update API documentation`

### PR Description
Include:
- What changes were made
- Why these changes were needed
- Related issues (use `Closes #123`)
- Screenshots (if UI changes)
- Testing performed

## Style Guide

### JavaScript/TypeScript

- Use ES6+ syntax
- 2-space indentation
- Use semicolons
- Prefer `const` over `let`, avoid `var`
- Use arrow functions when appropriate

```javascript
// Good
const getData = async () => {
  const result = await fetchData();
  return result;
};

// Avoid
var getData = function() {
  return fetchData();
};
```

### File Organization
```
src/
├── components/     # React/Vue components
├── utils/         # Utility functions
├── styles/        # CSS/SCSS files
├── types/         # TypeScript types
├── tests/         # Test files
└── index.ts       # Entry point
```

### Comments
- Write self-documenting code
- Use comments to explain **why**, not **what**
- Keep comments up-to-date with code

```javascript
// Good: Explains the intent
// Batch requests to avoid overwhelming the API
const batched Requests = [];

// Avoid: Redundant
// Set x to 5
const x = 5;
```

## Testing

### Write Tests
- Aim for >80% code coverage
- Test happy paths and edge cases
- Use descriptive test names

```typescript
describe('DataWidget', () => {
  it('should display data when loaded', () => {
    // test code
  });

  it('should show error message on fetch failure', () => {
    // test code
  });
});
```

### Run Tests
```bash
npm test              # Run all tests
npm test -- --watch  # Watch mode
npm test -- --coverage  # Coverage report
```

## Documentation

- Update README.md for user-facing changes
- Update CHANGELOG.md with version info
- Add JSDoc comments to public functions
- Update architecture docs if needed

## Getting Help

- **Questions**: Open a [GitHub Discussion](../../discussions)
- **Issues**: Check [existing issues](../../issues) before creating new ones
- **Security**: See [SECURITY.md](./SECURITY.md)
- **Chat**: Reach out to maintainers

## Recognition

Contributors will be recognized in:
- [README.md](./README.md) (list of contributors)
- [CHANGELOG.md](./CHANGELOG.md) (version release notes)
- GitHub contributors page

## License

By contributing, you agree that your contributions will be licensed under the same license as the project (MIT).

---

**Thank you for contributing to pi-dashboard!** 🎉

For more information, see [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md) and [SECURITY.md](./SECURITY.md).
