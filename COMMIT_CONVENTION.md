# Conventional Commits Guide

We use the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification to standardize commit messages.

## Format

```plaintext
<type>(optional-scope): <short description>

[optional body]

[optional footer]
```

---

## Examples

```plaintext
feat: add support for Gitea runner
fix: correct port mapping in Jellyfin
docs: update README with service structure
chore: add commitlint and husky for commit validation
```

---

## Allowed `<type>` values

| Type     | Description                                  |
|----------|----------------------------------------------|
| feat     | A new feature                                |
| fix      | A bug fix                                    |
| docs     | Documentation-only changes                   |
| style    | Code style changes (formatting, etc.)        |
| refactor | Code changes that neither fix nor add        |
| test     | Adding or updating tests                     |
| chore    | Maintenance tasks (build, deps, tooling...)  |

---

## Example with scope

```bash
feat(minio): add support for S3 bucket mounting
```

---
