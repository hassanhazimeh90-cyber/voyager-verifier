# Contributing

Thank you for your interest in contributing to Voyager Verifier! This guide will help you get started.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How to Contribute](#how-to-contribute)
- [Opening an Issue](#opening-an-issue)
- [Submitting a Pull Request](#submitting-a-pull-request)
- [Development Setup](#development-setup)
- [Coding Standards](#coding-standards)
- [Documentation](#documentation)
- [Community](#community)

## Code of Conduct

By participating in this project, you agree to maintain a respectful and inclusive environment. Be considerate, professional, and constructive in all interactions.

## How to Contribute

There are many ways to contribute to Voyager Verifier:

- **Report bugs** - Found a bug? Let us know by opening an issue
- **Suggest features** - Have an idea? Open an issue to discuss it
- **Fix issues** - Browse open issues and submit a fix
- **Improve documentation** - Help make our docs better
- **Write tests** - Increase code coverage and reliability

## Opening an Issue

**Before opening a pull request, please open an issue first.** This allows us to:

- Discuss the proposed changes
- Ensure the approach aligns with project goals
- Avoid duplicate work
- Provide feedback early in the process

### Bug Reports

When reporting a bug, please include:

- **Clear title** - Summarize the issue concisely
- **Description** - Detailed explanation of the problem
- **Steps to reproduce** - Specific steps to trigger the bug
- **Expected behavior** - What should happen
- **Actual behavior** - What actually happens
- **Environment** - OS, Rust version, dependency versions
- **Error messages** - Full error output or stack traces
- **Screenshots** - If applicable

### Feature Requests

When suggesting a feature, please include:

- **Use case** - Why is this feature needed?
- **Proposed solution** - How should it work?
- **Alternatives** - Other approaches you've considered
- **Implementation details** - Technical considerations if applicable

## Submitting a Pull Request

### Workflow

1. **Open an issue first** to discuss the changes
2. **Fork the repository** and create a branch from `main`
3. **Make your changes** following our coding standards
4. **Write or update tests** to cover your changes
5. **Update documentation** as needed
6. **Ensure tests pass** with `cargo test`
7. **Run linting** with `cargo lint`
8. **Format code** with `cargo fmt`
9. **Commit your changes** with clear, descriptive messages
10. **Push to your fork** and submit a pull request

### Pull Request Guidelines

- **Reference the issue** - Link to the issue your PR addresses
- **Clear description** - Explain what changes you made and why
- **Small, focused PRs** - Keep changes atomic and easy to review
- **One feature per PR** - Don't bundle unrelated changes
- **Tests included** - All new code should have tests
- **Documentation updated** - Keep docs in sync with code changes
- **CI must pass** - All checks must be green before merge

### Commit Messages

Write clear, descriptive commit messages:

```
Short summary (50 chars or less)

More detailed explanation if needed. Wrap at 72 characters.
Explain the problem this commit solves and why this approach
was chosen.

Fixes #123
```

## Development Setup

### Prerequisites

- Rust 1.70 or later
- Cargo
- Git

### Getting Started

1. Clone your fork:
   ```bash
   git clone https://github.com/YOUR_USERNAME/voyager-verifier.git
   cd voyager-verifier
   ```

2. Add upstream remote:
   ```bash
   git remote add upstream https://github.com/NethermindEth/voyager-verifier.git
   ```

3. Install dependencies:
   ```bash
   cargo build
   ```

4. Run tests:
   ```bash
   cargo test
   ```

5. Run the project:
   ```bash
   cargo run
   ```

### Keeping Your Fork Updated

```bash
git fetch upstream
git checkout main
git merge upstream/main
```

## Coding Standards

### Rust Style

- Follow standard Rust conventions and idioms
- Use `cargo fmt` to format code
- Address all `cargo lint` warnings
- Write idiomatic Rust code

### Code Quality

- **Write tests** - Aim for high test coverage
- **Handle errors properly** - Use `Result` and proper error types
- **Document public APIs** - Add doc comments to public items
- **Avoid unwrap/expect** - Handle errors gracefully
- **Keep functions focused** - Single responsibility principle
- **Use meaningful names** - Clear, descriptive variable and function names

### Testing

- Write unit tests for individual functions
- Add integration tests for workflows
- Test edge cases and error conditions
- Ensure all tests pass before submitting

## Documentation

See [Documentation Guidelines](./documentation.md) for detailed information on:

- Writing and updating documentation
- Building documentation locally
- Documentation structure and style

## Community

### Quick Links

- [GitHub Repository](https://github.com/NethermindEth/voyager-verifier)
- [Issue Tracker](https://github.com/NethermindEth/voyager-verifier/issues)
- [Pull Requests](https://github.com/NethermindEth/voyager-verifier/pulls)

### Getting Help

- Check existing documentation
- Search closed issues for similar problems
- Open a new issue if you need help

### Review Process

- Maintainers will review your PR as soon as possible
- Be responsive to feedback and questions
- Changes may be requested before merging
- Once approved, a maintainer will merge your PR

## License

By contributing to Voyager Verifier, you agree that your contributions will be licensed under the same license as the project.
