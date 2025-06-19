# File Browser

[File Browser](https://filebrowser.org/) is a lightweight and user-friendly web file manager that gives you access to files on your server from any browser.

## Features

- Drag & drop file uploads and downloads
- File previews, text editing, image viewer
- Authentication system and user management
- CLI and JSON API available
- Works great with mounted external folders

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

- Open the UI: <http://localhost:8084>
  - Default login: admin
  - Default password: admin (change it!)

## Notes

- You can mount any folder into /srv to expose it inside the web UI
- You may mount multiple folders if needed. They will appear under /srv in the File Browser UI.

Example:

```yaml
volumes:
  - /mnt/media:/srv/media
  - /home/user/files:/srv/userfiles
```

- The database (filebrowser.db) and config are stored in a Docker volume

## 📄 Docs

- <https://filebrowser.org/cli>
- <https://filebrowser.org/configuration>
