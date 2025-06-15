# MySQL

This is a standalone MySQL 9 container that can be used by other self-hosted services.

## Features

- Easy to connect from other Docker services
- Stores data in a Docker-managed volume
- Uses environment variables for configuration

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

**Volumes:** MySQL data is stored in mysql_data volume

## Integration

Other services can connect to this container by using:

- **Host:** mysql (Docker service name)
- **Port:** 3306
- **User/password** as defined in the .env file

Make sure the other service is in the same Docker network.

---

Official Docs : <https://hub.docker.com/_/mysql>
