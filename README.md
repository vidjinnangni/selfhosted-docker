# selfhosted-docker

A collection of `docker-compose.yaml` files to easily self-host popular open-source services.

[![License: MIT](https://img.shields.io/github/license/vidjinnangni/selfhosted-docker)](LICENSE)
[![Last Commit](https://img.shields.io/github/last-commit/vidjinnangni/selfhosted-docker)](https://github.com/ton-utilisateur/selfhosted-docker/commits/main)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/ton-utilisateur/selfhosted-docker/pulls)
[![Stars](https://img.shields.io/github/stars/vidjinnangni/selfhosted-docker?style=social)](https://github.com/ton-utilisateur/selfhosted-docker/stargazers)
[![Renovate enabled](https://img.shields.io/badge/renovate-enabled-brightgreen?style=flat-square)](https://github.com/apps/renovate)
[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg)](https://conventionalcommits.org)

---

## Table of Contents

- [Available Services](#available-services)
- [Requirements](#requirements)
- [Usage](#usage)
- [Docker Image Tags](#docker-image-tags)
- [Volume Paths](#volume-paths)
- [Contributions](#contributions)

---

## Available Services

Click on each link to view its `docker-compose.yaml` and setup instructions:

| Service              | Category     | Link                              |
|----------------------|--------------|-----------------------------------|
| File Browser         | Utilities    | [file_browser](./file_browser/)   |
| FreshRSS             | Content      | [freshrss](./freshrss/)           |
| Gitea                | DevOps       | [gitea](./gitea/)                 |
| Gitea Runner         | DevOps       | [gitea-act-runner](./gitea-act-runner/) |
| Homepage             | Dashboard    | [homepage](./homepage/)           |
| It-tools             | Utilities    | [it-tools](./it-tools/)           |
| Jellyfin             | Media        | [jellyfin](./jellyfin/)           |
| Jellyseerr           | Media        | [jellyseerr](./jellyseerr/)       |
| Kavita               | Media        | [kavita](./kavita/)               |
| MariaDB              | Database     | [mariadb](./mariadb/)             |
| MinIO                | Storage      | [minIO](./minIO/)                 |
| MySQL                | Database     | [mysql](./mysql/)                 |
| Nextcloud            | Storage      | [nextcloud](./nextcloud/)         |
| Nginx Proxy Manager  | Network      | [npm](./npm/)                     |
| pgAdmin              | Database     | [pgadmin](./pgadmin/)             |
| Pi-hole              | Network      | [pihole](./pihole/)               |
| Portainer            | DevOps       | [portainer](./portainer/)         |
| PostgreSQL           | Database     | [postgresql](./postgresql/)       |
| qBittorrent          | Media        | [qbittorrent](./qbittorrent/)     |
| Vaultwarden          | Security     | [vaultwarden](./vaultwarden/)     |
| Wallos               | Utilities    | [wallos](./wallos/)               |

> [!NOTE]
> **More services will be added over time.** Feel free to contribute via pull requests!

---

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
docker compose up -d
```

> [!TIP]
> If the folder contains a .env file, copy it and adjust settings before starting the container.

## Docker Image Tags

This repository uses versioned Docker image tags (**SemVer**) instead of latest to ensure consistency and reproducibility.

Additionally, all images are pinned with **SHA256** digests using _Renovate_.
This guarantees that pulling the same docker-compose.yaml always results in the same image build, even if upstream changes occur.

Example:

```yaml
image: nextcloud@sha256:9f0aab9e...
```

> _Renovate_ automatically checks for updates and opens pull requests when a new version (with updated digest) is available.

## Volume Paths

> [!NOTE]
> The local volume paths in each docker-compose.yaml (like ./data:/data, ./db:/var/lib/mysql, etc.) are only examples.
> You can adapt the paths to whatever suits your environment, for instance:

```yaml
- /mnt/docker-data/nextcloud:/data
- /srv/services/vaultwarden/data:/data
- ~/docker/nginx-proxy-manager/letsencrypt:/etc/letsencrypt
```

Make sure that:

- The folders exist or will be created automatically
- The Docker engine has access to them

---

## Contributions

Pull requests are welcome!

To contribute:

- Create a new folder under services/
- Add a clean, minimal `docker-compose.yaml`
- Optionally include a `.env` example file and a short `README.md`
- Avoid including reverse proxy setup unless strictly required

Let’s build a simple, useful reference for the self-hosting community 🚀
