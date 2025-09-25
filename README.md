# 🖥️ MeshCentral on Coolify (Docker Compose)

This repository provides a **Coolify-ready Docker Compose configuration** for running [MeshCentral](https://github.com/Ylianst/MeshCentral), a powerful remote management platform for devices and servers.  

## 🚀 Features
- **Seamless Coolify integration** – deploy directly from this `docker-compose.yml`  
- **Production-ready** with `NODE_ENV=production`  
- **Reverse proxy + TLS** handled by Coolify’s built-in domain and SSL management  
- **Security hardened** defaults:
  - Session key regenerated on each startup  
  - Account creation disabled (`ALLOW_NEW_ACCOUNTS=false`)  
  - Trusted proxy set to `all` for reverse-proxy compatibility  
- **Persistent storage** via volumes for:
  - MeshCentral configuration & data  
  - User file uploads  
  - Backups  
  - Web customisations  

## 📦 Deployment
1. Add this repository as a **Git Source** in your self-hosted Coolify instance.  
2. Configure the required environment variables (e.g. `SERVICE_URL_MESHCENTRAL`, `SERVICE_FQDN_MESHCENTRAL`).  
3. Deploy with a single click – Coolify automatically manages SSL certificates, domain binding, and orchestration.
4. Login to the meshcontainer and edit the config.json settings
5. Then edit the compose file and change "DYNAMIC_CONFIG=false" to stop overwriting config.json
6. Restart the containers.

> ℹ️ **Note**: This setup is designed for **self-hosted Coolify** with wildcard subdomains already configured.
