# MariaDB

[MariaDB](https://mariadb.org) is a popular drop-in replacement for MySQL. This container runs a standalone MariaDB 10.x server you can connect other services to.

## Features

- Persistent storage via Docker volume
- Easily reusable by other containers (Nextcloud, etc.)
- Configurable via `.env` file

## Folder Structure

```bash
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

## Connection Details

- **Host:** mariadb (Docker service name)
- **Port:** ${MARIADB_PORT} (default: 3306)
- **Database/user/password:** defined in .env

Make sure the other service is on the same Docker network.

## Data Persistence

Data is stored in the mariadb_data volume.

---

Docs : <https://hub.docker.com/_/mariadb>
