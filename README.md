# maintenance-cbt-page

Static maintenance page served by Nginx.

## Deployment

This repository now includes `docker-compose.yml` for Dokploy or any Compose-based deployment.

### Docker Compose

```bash
docker compose up --build -d
```

The Compose service only exposes container port `80` internally and does not bind a fixed host port.
This avoids host port conflicts in Dokploy (especially when using the Nginx template).

If you need direct local host-port access outside Dokploy, add a local Compose override:

```bash
cat > docker-compose.override.yml <<'EOF'
services:
  maintenance-cbt-page:
    ports:
      - "8080:80"
EOF

docker compose up --build -d
```
