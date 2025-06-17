# Homepage

[Homepage](https://github.com/gethomepage/homepage) is a modern, customizable dashboard for your self-hosted services. It helps you visualize and access your running containers or external services from a single clean web interface.

## Features

- Beautiful and responsive web UI
- Groups services with icons, status, and links
- Integration with Docker, Kubernetes, and more
- Supports bookmarks, widgets, and custom layouts
- Simple configuration via YAML files

## Folder Structure

```plaintext
├── docker-compose.yaml
├── config/
│   ├── settings.yaml
│   ├── services.yaml
│   ├── bookmarks.yaml
│   └── …
```

> 📁 You can adapt the config path (`./config`) in the compose file to whatever suits your setup.

## Usage

Homepage uses YAML files for configuration. Key files include `settings.yaml`, `services.yaml`, `bookmarks.yaml`, `custom.css`, and `widgets.yaml`, which respectively handle core settings, service definitions, bookmarks, custom styling, and widget configurations.

- Start the service:

```bash
docker compose up -d
```

- Access the dashboard at <http://localhost:3000>
- Edit the config files under the `config/` folder.

> [!NOTE]
>
> - The Docker socket is mounted to allow container status integration. Remove it if not needed.
> - Config files are hot-reloaded — no need to restart the container on change.

---

## Documentation

- Homepage site: <https://gethomepage.dev>
- Configuration guide: <https://gethomepage.dev/latest/configs/>
