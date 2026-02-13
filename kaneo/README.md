# Kaneo

[Kaneo](https://github.com/usekaneo/kaneo) (/kəˈneɪ.oʊ/) is a **project management tool** that gets out of your way. It is designed to be a **simple**, **yet powerful tool** for managing your projects. It works for you instead of you working for it.

## Features

- Tasks and boards (Kanban style)
- Project and workspace organization
- Markdown notes and descriptions
- Collaboration-friendly interface
- Clean, fast, and intuitive design
- Fully self-hosted with PostgreSQL + Redis

## Folder Structure

```plaintext
kaneo/
├── docker-compose.yaml
├── .env
└── README.md
```

## Usage

- Navigate to the folder and configure environment

Copy, edit `.env` file and set your: database credentials, port bindings...

- Run:

```bash
docker compose up -d
```

- And open <http://localhost:5173>

---

See [full documentation](https://kaneo.app/docs/core) for detailed setup instructions, environment variable configuration, and troubleshooting guides.
