# MinIO

[MinIO](https://min.io/) is a high-performance, self-hosted object storage server, fully compatible with Amazon S3 APIs. It’s ideal for storing files, media, backups, and more.

## Features

- S3-compatible API
- High performance and scalability
- Web UI and CLI support
- Perfect for backups, cloud-native apps, or file sharing

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

- Access the web UI: <http://localhost:9001>

Log in with `${MINIO_ROOT_USER}` and `${MINIO_ROOT_PASSWORD}`.

---

**📄 Docs:** <https://docs.min.io>
