# maintenance-cbt-page

Static maintenance page served by Nginx.

## Deployment

This repository now includes `docker-compose.yml` for Dokploy or any Compose-based deployment.

### Docker Compose

```bash
docker compose up --build -d
```

If port `80` is already in use, set `PORT` before starting Compose, for example:

```bash
PORT=8080 docker compose up --build -d
```
