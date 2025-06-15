# selfhosted-docker

A collection of `docker-compose.yaml` files to easily self-host popular open-source services.

[![License: MIT](https://img.shields.io/github/license/vidjinnangni/selfhosted-docker)](LICENSE)
[![Last Commit](https://img.shields.io/github/last-commit/vidjinnangni/selfhosted-docker)](https://github.com/ton-utilisateur/selfhosted-docker/commits/main)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/ton-utilisateur/selfhosted-docker/pulls)
[![Stars](https://img.shields.io/github/stars/vidjinnangni/selfhosted-docker?style=social)](https://github.com/ton-utilisateur/selfhosted-docker/stargazers)

## Requirements

- Docker
- Docker Compose
- Linux/Unix/Windows machine (VPS, home server, NAS, etc.)

## Usage

We suggest organizing your services like this:

```plaintext
/opt/selfhost/docker/
├── services/
│   ├── vaultwarden/
│   │   └── docker-compose.yaml
│   ├── nextcloud/
│   ├── jellyfin/
│   └── ...
│
```

To run a service:

```bash
cd /opt/selfhost/docker/services/vaultwarden
docker-compose up -d
```

> [!TIP]
> If the folder contains a .env.example file, copy it to .env and adjust settings before starting the container.

## Contributions

Pull requests are welcome!

To contribute:

- Create a new folder under services/
- Add a clean, minimal docker-compose.yaml
- Optionally include a .env.example file and a short README.md
- Avoid including reverse proxy setup unless strictly required

Let’s build a simple, useful reference for the self-hosting community 🚀
