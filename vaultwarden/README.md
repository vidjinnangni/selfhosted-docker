# Vaultwarden

[Vaultwarden](https://github.com/dani-garcia/vaultwarden) is a lightweight, self-hosted implementation of the Bitwarden password manager backend, compatible with official Bitwarden clients.

## Features

- Compatible with Bitwarden apps (web, mobile, desktop, browser)
- Lightweight and efficient (Rust-based)
- Easy to deploy with Docker
- Can use SQLite, PostgreSQL, or MySQL

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

- Access the Web UI at: <http://localhost:8082>

## Admin Panel (optional)

Set `ADMIN_TOKEN` in .env to enable the /admin panel.

## Data Persistence

All user data and settings are stored in a volume named vw_data.

📄 **Official Docs:** <https://github.com/dani-garcia/vaultwarden/wiki>
