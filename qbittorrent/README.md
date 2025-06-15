# qBittorrent

[qBittorrent](https://www.qbittorrent.org/) is a powerful and open-source BitTorrent client. This setup provides a web interface for managing downloads.

## eatures

- Full-featured Web UI (based on Qt)
- Supports watch folders, labels, RSS, speed limits, etc.
- Ideal for use with other tools like Radarr/Sonarr

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

- **Access the Web UI at:** <http://localhost:8081>
- **Default login: admin:** Default password: adminadmin (change it on first login).

## 📂 Data

- Downloads will go to the directory defined in ${DOWNLOADS_DIR}.
- Config is persisted in qbittorrent_config volume.
- <https://github.com/qbittorrent/qBittorrent/wiki/Web-UI>
