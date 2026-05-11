# maintenance-cbt-page

Static maintenance page served by Nginx.

## Deployment

This repository now includes `docker-compose.yml` for Dokploy or any Compose-based deployment.

### Docker Compose

```bash
docker compose up --build -d
```

By default, Compose maps host port `8080` to container port `80` to avoid collisions on hosts already using port `80`.

To use a different host port, set `PORT` before starting Compose, for example:

```bash
PORT=9090 docker compose up --build -d
```
