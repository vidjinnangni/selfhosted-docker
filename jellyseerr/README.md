# Jellyseerr

[Jellyseerr](https://github.com/Fallenbagel/jellyseerr) is a free and open-source request management system for your Jellyfin media library.

## Features

- Request movies and TV shows via a modern web UI
- Built-in user authentication (can connect to Jellyfin)
- Admin approval workflows and quotas
- Integrates with Jellyfin and downloaders like Radarr/Sonarr

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

- Access Jellyseerr at: <http://localhost:5055>

## Authentication

You can log in with your Jellyfin account or set up a local admin user on first launch.

---

**Docs:** <https://github.com/Fallenbagel/jellyseerr/wiki>
