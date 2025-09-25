# 🖥️ MeshCentral on Coolify (Docker Compose)

This repository contains a **Coolify-ready Docker Compose file** for deploying [MeshCentral](https://github.com/Ylianst/MeshCentral), a remote management platform for devices and servers.  

## 🚀 Features
- **Coolify integration** – drop this `docker-compose.yml` into Coolify for one-click deployment  
- **Production-ready setup** with `NODE_ENV=production`  
- **Reverse proxy + TLS support** via Coolify’s built-in domain & SSL management  
- **Security hardened** by default:
  - Session key regeneration on startup  
  - New account creation disabled (`ALLOW_NEW_ACCOUNTS=false`)  
  - Trusted proxy set to `all` for reverse-proxy compatibility  
- **Persistent storage** with dedicated volumes:
  - MeshCentral configuration/data  
  - User file uploads  
  - Automated backups  
  - Web customisations  

## 📦 Deployment
1. Add this repository as a **Git Source** in Coolify.  
2. Configure environment variables (e.g. `SERVICE_URL_MESHCENTRAL`, `SERVICE_FQDN_MESHCENTRAL`).  
3. Deploy with a single click – Coolify will handle SSL certificates, domain binding, and container orchestration.  

## 🔑 Example
```bash
docker compose up -d
