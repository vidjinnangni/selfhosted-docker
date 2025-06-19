# Pi-hole

[Pi-hole](https://pi-hole.net/) is a network-wide ad blocker that acts as a local DNS server, blocking ads and trackers for all devices in your network.

## Features

- Blocks ads, trackers, telemetry at the DNS level
- Web UI with real-time statistics
- Works with any device (TVs, phones, IoT, etc.)
- Can replace your router’s DNS or act as DHCP

## Folder Structure

```plaintext
├── docker-compose.yaml
├── .env
└── README.md
```

> 📝 Note: You may need to run Pi-hole on a specific network or interface depending on your system (e.g. `macvlan` or `host` mode). The config below works in bridge mode for testing, but production use may differ.

## Usage

- Navigate to the folder
- Open the `.env` file and configure it
- And run:

```bash
docker compose up -d
```

- Access the Web UI at: <http://localhost:8083/admin>

## Default Access

- Admin password is set via .env (WEBPASSWORD)

---

**📄 Docs:** <https://docs.pi-hole.net>
