# Contributing to saidsef/saidsef

Thank you for your interest in contributing! This repository contains:

1. My GitHub profile README
2. Reusable GitHub Actions workflows for the saidsef organization

## How to Contribute

### Reporting Issues

- Use GitHub Issues for bug reports and feature requests
- For security issues, see [SECURITY.md](./SECURITY.md)

### Workflow Improvements

When contributing to workflows:

1. **Test your changes**: If possible, test in a fork first
2. **Follow conventions**:
   - Use `workflow_call` for reusable workflows
   - Set `timeout-minutes: 5` for jobs
   - Include concurrency controls
   - Pin action versions (not `@master` or `@main`)
3. **Update documentation**: If you add features, update relevant documentation

### Code Style

- YAML: 2-space indentation
- Action versions: use `@v6` format (or newer)
- Names: descriptive, use kebab-case

### Commit Messages

Follow conventional commits:

- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation changes
- `chore:` Maintenance tasks

Example: `feat(workflows): add OpenTofu 1.12 support`

### Pull Request Process

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Ensure workflows pass (if applicable)
5. Submit a PR with clear description

## Questions?

Open an issue or reach out via LinkedIn.
