# Linkwarden

[Linkwarden](https://github.com/linkwarden/linkwarden) is a self-hosted bookmark manager to organize and preserve useful links.

## Features

- Organize bookmarks with tags and notes
- Archive web pages locally
- Built with Next.js and PostgreSQL
- Easy authentication with NextAuth

## Folder structure

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

- Visit <http://localhost:3000> (or your configured port).

## Notes

- Linkwarden requires NEXTAUTH_SECRET for secure sessions.
- All data is stored locally under ./data and ./pgdata.

---

**📄 Docs:** <https://docs.linkwarden.app/>
