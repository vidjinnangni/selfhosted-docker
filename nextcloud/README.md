# Nextcloud

[Nextcloud](https://nextcloud.com) is a self-hosted productivity platform that lets you store, share, and manage files, calendars, contacts, and more.

## Features

- File synchronization and sharing
- Web interface + desktop & mobile apps
- Collaborative apps (Notes, Calendar, Tasks, Talk, etc.)
- Extensible with plugins

## Folder Structure

```plaintext
├── docker-compose.yaml
├── .env
└── README.md
```

## Usage

- Navigate to the folder
- Open the `.env` file and configure it
- And run:

```bash
docker compose up -d
```

- Access Nextcloud at: <http://localhost:8080>
- Complete the web-based setup (admin account, database config)

## Data Storage

- Nextcloud data is stored in the nextcloud_data volume.
- MariaDB data is stored in the db_data volume.

## Reverse Proxy

This setup does not include HTTPS.
You can use any reverse proxy (Traefik, Nginx Proxy Manager, etc.) to enable HTTPS and route traffic.

---

**Official Docs:** <https://nextcloud.com/blog/how-to-install-the-nextcloud-all-in-one-on-linux/>
