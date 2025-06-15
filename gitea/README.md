# Gitea

[Gitea](https://gitea.io) is a lightweight, self-hosted Git service similar to GitHub, GitLab, or Bitbucket — easy to set up and efficient to run on minimal resources.

## Features

- Web UI for repositories, issues, pull requests, etc.
- Built-in SSH server
- Lightweight and fast
- Easy to deploy with Docker

## Docker Setup

This folder contains a `docker-compose.yaml` file to quickly get Gitea running locally.

## Folder structure

```bash
├── docker-compose.yaml
└── README.md
```

## Usage

- Navigate to the service folder, and run:

```bash
docker compose up -d
```
- Access the web interface at: http://localhost:3000
- The default SSH port is mapped to localhost:222 for Git over SSH.

## Configuration

All data is stored in a Docker-managed volume named gitea_data. On first launch, Gitea will guide you through the initial setup in the browser.

You can customize the UID, GID, and root URL in the environment section of the compose file.

## Stop and remove the containers

```bash
docker compose down
```

Official Docs: https://docs.gitea.com/next/installation/install-with-docker
