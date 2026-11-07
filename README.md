# infra

Reverse proxy et services de phrolonyx.com.

- **Caddy** : point d'entrée unique (80/443), HTTPS automatique (Let's Encrypt)
- **Docker Compose** : chaque service rejoint le réseau `web` sans publier de port
- `site/` : landing page statique servie par Caddy

## Déploiement
    git pull
    docker compose up -d
    docker compose exec -w /etc/caddy caddy caddy reload   # après un changement du Caddyfile
