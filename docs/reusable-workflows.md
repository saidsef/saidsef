# Reusable Workflows Usage Guide

This repository provides reusable GitHub Actions workflows for the saidsef organization.

## Available Workflows

### Terraform Validation (`tf-validate.yaml`)

Validates Terraform configurations across multiple versions (1.3.x - 1.14.x).

**Usage:**

```yaml
jobs:
  terraform:
    uses: saidsef/saidsef/.github/workflows/tf-validate.yaml@main
```

**Inputs:**

| Name | Default | Description |
|------|---------|-------------|
| `start-version` | `'3'` | Starting Terraform version (1.3.x) |
| `end-version` | `'14'` | Ending Terraform version (1.14.x) |

**Outputs:**

| Name | Description |
|------|-------------|
| `versions` | JSON array of tested Terraform versions |

**Requirements:**
- `examples/complete/` and `examples/remote/` directories must exist

---

### OpenTofu Validation (`tofu-validate.yaml`)

Validates OpenTofu configurations across multiple versions (1.6.x - 1.11.x).

**Usage:**

```yaml
jobs:
  opentofu:
    uses: saidsef/saidsef/.github/workflows/tofu-validate.yaml@main
```

**Inputs:**

| Name | Default | Description |
|------|---------|-------------|
| `start-version` | `'6'` | Starting OpenTofu version (1.6.x) |
| `end-version` | `'11'` | Ending OpenTofu version (1.11.x) |

**Outputs:**

| Name | Description |
|------|-------------|
| `versions` | JSON array of tested OpenTofu versions |

**Requirements:**
- `examples/complete/` and `examples/remote/` directories must exist

---

### Security Scanning (`tf-security.yaml`)

Scans Terraform with Checkov and uploads SARIF results to GitHub Security tab.

**Usage:**

```yaml
jobs:
  security:
    uses: saidsef/saidsef/.github/workflows/tf-security.yaml@main
    permissions:
      security-events: write
      contents: read
```

**Permissions Required:**
- `security-events: write` - To upload SARIF results
- `contents: read` - To checkout repository

---

### Tag & Release (`tag-release.yaml`)

Auto-generates semantic version tags based on commit analysis.

**Usage:**

```yaml
on:
  push:
    branches: [main]

jobs:
  release:
    uses: saidsef/saidsef/.github/workflows/tag-release.yaml@main
    permissions:
      contents: write
```

**Features:**
- Automatic semantic versioning (major/minor/patch)
- GitHub release generation
- Change classification based on git diff:
  - **Major**: Breaking changes (resource deletion, destructive changes, removed functions/classes)
  - **Minor**: New features (new resources, variables, outputs, functions, dependencies)
  - **Patch**: All other changes

---

### Dependency Review (`dependency-review.yaml`)

Scans PR dependencies for vulnerabilities.

**Usage:**

```yaml
jobs:
  review:
    uses: saidsef/saidsef/.github/workflows/dependency-review.yaml@main
```

**Inputs:**

| Name | Default | Description |
|------|---------|-------------|
| `allow-ghsas` | `true` | Allow specific GitHub Security Advisories |
| `comment-summary-in-pr` | `'always'` | Comment summary in PR |
| `fail-on-severity` | `'high'` | Minimum severity to fail |

---

### Pre-commit (`pre-commit.yaml`)

Runs pre-commit hooks via GitHub Actions.

**Usage:**

```yaml
jobs:
  precommit:
    uses: saidsef/saidsef/.github/workflows/pre-commit.yaml@main
```

**Hooks Included:**
- `terraform_fmt` - Format check
- `terraform_tflint` - Lint with tflint rules
- `terraform_validate` - Validation
- `check-yaml` - YAML validation
- `detect-private-key` - Private key detection
- `trailing-whitespace` - Whitespace cleanup

---

### Auto-approve (`auto-approve.yaml`)

Auto-approves PRs (requires write permissions).

**Usage:**

```yaml
jobs:
  approve:
    uses: saidsef/saidsef/.github/workflows/auto-approve.yaml@main
    secrets:
      GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

**Permissions Required:**
- `contents: write` - To approve PRs

---

### Attestation (`tf-attest.yaml`)

Creates build provenance attestations for `.tf` files.

**Usage:**

```yaml
jobs:
  attest:
    uses: saidsef/saidsef/.github/workflows/tf-attest.yaml@main
    permissions:
      contents: read
      id-token: write
      attestations: write
```

**Note:** Only runs on `main` branch.

## Version Pinning

For production stability, pin to a specific release tag:

```yaml
uses: saidsef/saidsef/.github/workflows/tf-validate.yaml@v1.0.0
```

Or use a SHA for maximum security:

```yaml
uses: saidsef/saidsef/.github/workflows/tf-validate.yaml@abc123def456...
```

## Best Practices

1. **Pin versions**: Always use `@main` or a pinned version/tag, never `@<branch>`
2. **Minimal permissions**: Grant only the permissions required for the workflow
3. **Test first**: Test workflows in a non-production repository before adopting
4. **Monitor updates**: Watch for new releases and security updates
