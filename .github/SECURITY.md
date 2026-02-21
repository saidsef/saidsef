# Security Policy

## Supported Versions

As this is a personal GitHub profile repository with reusable workflows, security updates are applied as soon as they are available.

## Reporting a Vulnerability

If you discover a security vulnerability in any of the workflows or configurations in this repository, please report it responsibly:

1. **Do not** open a public issue
2. Use GitHub's private vulnerability reporting
3. Include:
   - Description of the vulnerability
   - Steps to reproduce
   - Potential impact
   - Suggested fix (if any)

## Security Measures

This repository implements the following security practices:

- **Dependency Management**: Dependabot configured for weekly updates
- **Action Pinning**: All GitHub Actions are pinned to specific versions
- **Minimal Permissions**: Workflows use least-privilege permissions
- **Security Scanning**: Checkov and tfsec for IaC security
- **SARIF Uploads**: Security findings are uploaded to GitHub Security tab

## Security Scanning

All reusable workflows include:

- Terraform/OpenTofu validation
- TFLint for code quality
- Checkov for security policy compliance
- tfsec for Terraform security scanning
