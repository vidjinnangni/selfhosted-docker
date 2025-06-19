# Portainer

[Portainer](https://www.portainer.io/) is a lightweight management UI for Docker, Docker Swarm, and Kubernetes. It allows you to manage containers, images, volumes, networks, and more through a browser.

## Features

- Manage Docker environments (local or remote)
- Container and stack management
- Image pulling, volume and network creation
- User authentication and role-based access
- Agent mode for remote nodes

## Folder Structure

```bash
├── docker-compose.yaml
└── README.md
```

## Usage

- Navigate to the folder, and run:

```bash
docker compose up -d
```

- Access the UI:
  - <http://localhost:9443> (HTTPS)
  - <http://localhost:9000> (HTTP — disabled by default in this config)

On first launch, you’ll be asked to create an admin user.

## Security

- The web interface is served via HTTPS on port 9443.
- No login exists by default — you must define one on first visit.

---

**📄 Docs:** <https://docs.portainer.io>
