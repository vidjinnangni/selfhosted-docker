# Kavita

[Kavita](https://github.com/Kareadita/Kavita) is a fast, self-hosted digital library for comics, manga, and ebooks. It’s designed to organize and serve your reading collection with a rich web UI.

## Features

- Scan and index comics/manga/ebooks by folder
- Series tracking, metadata, and cover art
- Reader with bookmarks and reading progress
- Web-based, fast and mobile-friendly

## Folder Structure

```plaintext
├── docker-compose.yaml
└── README.md
```

## Usage

- Navigate to the folder, and run:

```bash
docker compose up -d
```

- Access the UI: <http://localhost:5000>

## Notes

- You can mount one or multiple folders for different types of media (e.g., /manga, /comics, /books).
- Inside the container, each folder should map to its corresponding location (/manga, /comics, /books).
- The path /kavita/config is required and must not be changed, as it stores settings and user data.
- On first launch, you’ll be prompted to create an admin account and set up your libraries.

---

**📄 Docs:** <https://wiki.kavitareader.com/>
