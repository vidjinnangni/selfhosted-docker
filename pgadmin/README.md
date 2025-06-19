# pgAdmin

[pgAdmin](https://www.pgadmin.org/) is the most popular and feature-rich open source administration and development platform for PostgreSQL.

## Features

- Full-featured web interface for PostgreSQL
- Manage multiple servers
- SQL editor with autocompletion
- Query results, statistics, backups, and more

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

- Access pgAdmin at: <http://localhost:5050>

## Login

- Email: ${PGADMIN_DEFAULT_EMAIL}
- Password: ${PGADMIN_DEFAULT_PASSWORD}

---

**📄 Docs:** <https://www.pgadmin.org/docs/>
