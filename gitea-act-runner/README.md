# Gitea with Runner

This service runs a standalone [Gitea Actions runner](https://docs.gitea.com/usage/actions/overview) that connects to an existing Gitea instance and executes workflows.

## Features

- Self-hosted CI runner for Gitea Actions
- Compatible with GitHub Actions workflows
- Docker-based job execution
- Auto-registration on startup

## Folder structure

```plaintext
├── docker-compose.yaml
├── .env
└── README.md
```

## Usage

> [!CAUTION]
> You need an active Gitea instance with Actions enabled.

### Obtain a Registration Token

- Navigate to your Gitea instance.
- Depending on the desired scope (instance, organization, or repository), go to the respective settings page (e.g., /admin/actions/runners for instance-level).
- Generate a new runner registration token and replace your_registration_token in the docker-compose.yml file with this token.

### Start the Runner

- Navigate to the folder
- Open the `.env` file and configure it
- And run:

```bash
docker compose up -d
```

- Navigate to your Gitea instance. Check your Gitea instance's runner settings page to confirm that the newly started runner is registered and active.

## Test workflow example

To verify that the runner is working, create a file in your Gitea repository at:

```plaintext
.gitea/workflows/ci.yml
```

With the following content:

```yaml
name: CI Test

on:
  push:
    branches:
      - main

jobs:
  hello-world:
    runs-on: docker
    steps:
      - name: Print hello
        run: echo "✅ Gitea Actions runner is working!"

```

Push to your main branch.
If the runner is correctly registered, the workflow will be executed and show logs in the UI.

---

**📄 Documentation:** <https://docs.gitea.com/usage/actions/act-runner>
