# PostgreSQL

This is a standalone PostgreSQL 15 container, which can be used as a shared database service for other self-hosted applications.

## Features

- Stores data in a Docker-managed volume
- Uses environment variables for configuration
- Can be reused by other containers (e.g. Gitea, Paperless-NGX)

## Folder Structure

```plaintext
├── docker-compose.yaml
├── .env
└── README.md
```

## Usage

- Copy the `.env` file and configure it
- Navigate to the folder, and run:

```bash
docker compose up -d
```

## Connection Info

- **Host:** postgresql (Docker service name)
- **Port:** ${POSTGRES_PORT} (default: 5432)
- **User / Password** from .env

## Volumes

Data is stored in a Docker volume named postgres_data.

---

**Official Docs:** <https://hub.docker.com/_/postgres>
