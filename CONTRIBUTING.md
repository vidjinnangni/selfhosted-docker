# Contributing to selfhosted-docker

Thanks for your interest in contributing! This repository provides clean, simple `docker-compose.yaml` files for popular self-hostable services.

Please follow these guidelines to ensure consistency and quality.

---

## How to contribute

### 1. Clone the Repository

```bash
git clone https://github.com/vidjinnangni/selfhosted-docker.git
cd selfhosted-docker
```

### 2. Add your service

- Create a new folder under /services/ with a clear name:

```plaintext
/services/
└── your-service-name/
    ├── docker-compose.yaml
    ├── .env                  # Optional
    └── README.md             # Recommended
```

Your docker-compose.yaml should:

- Be minimal and clean
- Use versioned image tags (semver)
- Pin image with SHA256 digest
- Avoid hardcoding absolute volume paths
- Avoid adding Traefik or Nginx unless strictly required
- Optional: include a small README.md with:
  - A short description of the service
  - Any post-deploy instructions (e.g., setup admin account)

---

**Tips for consistency:**

- Use 2-space indentation for YAML
- Use lowercase folder names with no spaces
- Use .env if your service depends on env vars
- Prefer Docker volumes or relative paths for bind mounts

---

### 3. Test before submitting

Make sure you:

- Run docker compose up -d and verify the service starts
- Avoid leaving unused volumes, ports, or placeholders
- Clean up unnecessary comments

### 4. Submit a Pull Request

- Fork the repository
- Push your branch
- Open a pull request against main
- Use Conventional Commits for your commit messages (e.g. feat: add paperless service)

---

## 🤝 Let’s build together

Feel free to open issues, suggest improvements, or request services you’d like to see.

Thanks for helping build a great resource for the self-hosting community 🚀
