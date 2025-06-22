# n8n

This service runs [n8n](https://n8n.io/), an extendable workflow automation tool that lets you connect apps and automate tasks.

## Features

- Self-hosted automation platform
- Visual workflow builder
- Basic Auth enabled by default
- Data persistence
- Easily extensible with community integrations

## Folder structure

```plaintext
├── docker-compose.yaml
├── .env
└── README.md
```

## Usage

> [!NOTE]
> Ensure Docker is installed and available on your system.

- Create or edit the .env file
- Start the service

```bash
docker compose up -d
```

The interface will be available at <http://localhost:5678> (or your configured port).

- Use the credentials configured in your `.env` file (N8N_BASIC_AUTH_USER / PASSWORD).

## Data persistence

All workflows and credentials are stored in `./data`.

> [!TIP]
> Make sure to back up this folder regularly.

---

**📄 Documentation:** <https://docs.n8n.io/>
