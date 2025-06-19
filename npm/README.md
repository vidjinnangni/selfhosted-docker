# Nginx Proxy Manager

[Nginx Proxy Manager](https://nginxproxymanager.com/) provides a simple and powerful web interface to manage Nginx reverse proxy hosts, SSL certificates, redirections, streams, and more.

## Features

- Web UI for managing proxy rules
- Built-in Let's Encrypt certificate support
- Access control, redirects, streaming
- Great alternative to Traefik for simple use cases

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

- **Access the UI:** <http://localhost:81>
- **Default login:** <admin@example.com>
- **Default password:** changeme

Immediately after logging in with this default user you will be asked to modify your details and change your password.

You can change defaults with:

```yaml
    environment:
      - INITIAL_ADMIN_EMAIL: my@example.com
      - INITIAL_ADMIN_PASSWORD: mypassword1
```

## Data

Configuration and SSL certs are stored in Docker volumes

---

**Docs:** <https://nginxproxymanager.com/guide/>
