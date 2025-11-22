# Family Server

This repository contains the infrastructure and documentation for a self-hosted family server.

## Repository content

### Ansible Playbooks (`ansible/`)

- `setup-server.yaml` - basic server configuration (Docker, Tailscale, Fish Shell)
- `setup-permissions.yaml` - file permissions and Samba configuration
- `setup-backups.yaml` - Backup system (Restic, Rclone)
- `files/` - configuration files (Samba, Rclone, backup scripts)

### Docker configurations (`docker/`)

- `immich/` - Immich Docker Compose
- `jellyfin/` - Jellyfin Docker Compose
- `caddy/` - Caddy reverse proxy with Dockerfile

### Documentation (`vitepress/`)

- VitePress-based documentation
- Admin documentation (`docs/admin/`)
- User documentation (`docs/user/`)

## Start VitePress

The documentation is provided with VitePress. How to start the local development server:

```bash
mise docs
```

The documentation can then be accessed at `http://localhost:5173`.

## Setup

For the initial setup of the project:

```bash
mise setup
```
