# Jellyfin

[Jellyfin](https://jellyfin.org) is a free and open-source media server that lets you stream your movies, TV shows, music, and more to any device.

## Features

- Stream locally or over the web
- Native apps for Android, iOS, smart TVs, etc.
- Transcoding support
- No tracking, no ads, fully open-source

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

Access the web interface: <http://localhost:8096>

## Volumes

- **config:** Jellyfin server settings, metadata, etc.
- **cache:** Transcoding cache
- **media:** Your actual media (mount your own path)

---

**Official Docs:** <https://jellyfin.org/docs/>
