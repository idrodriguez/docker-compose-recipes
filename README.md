# Homelab Docker Compose Setup

Welcome to my GitHub repository where I store all the **docker-compose.yml** files for my self-hosted homelab running on an ArchLinux NUC server. This repository is a backup of my current infrastructure, which I use to manage and run several self-hosted services.

---

## 🌐 Domain and Dynamic DNS Setup

Some services in my homelab are accessible via my registered domain **mydomain.example**. I use **ddclient** to dynamically update my public IP address in **Cloudflare**, ensuring that my domain always points to the correct IP address, even if it changes.

---

## 🛠️ System Overview

This setup is designed to be lightweight, running on an **ArchLinux** installation with minimal additional software to maximize CPU and memory efficiency. The only additional tools installed beyond Docker are essential utilities to manage system services and performance.

Key components of the system:
- **Operating System**: ArchLinux
- **Hardware**: Intel NUC7i5bnb
- **Services Managed**: Docker, ddclient (for dynamic DNS)

---

## 🖥️ Installed Services

Here's a list of the services I'm running in Docker containers on this server:

1. **AdGuard Home** - Network-wide ad blocker.
2. **Grafana** - Visualization tool for monitoring various metrics.
3. **Ghostfolio** - Open-source wealth management tool.
4. **Immich** - Self-hosted photo and video backup solution.
5. **Paperless-NGX** - Document management and archiving.
6. **Portainer** - Docker container management GUI.
7. **Presearch** - Decentralized search engine.
8. **Watchtower** - Automatic updates for Docker containers.
9. **Traefik** - Reverse proxy for managing external access to services.
10. **WireGuard** - Secure VPN server.
11. **VaultWarden** - Password Manager API for bitwarden client.

Each service is configured via its own **docker-compose.yml** file, with settings managed primarily through `.env` files for better modularity and security.

---

## 🛡️ Network and Security

- **WireGuard** is used to provide secure remote access to my homelab from outside the network.
- **Traefik** is configured to handle reverse proxying and routing to the services securely over HTTPS.

---

## 🤝 Contributions and Suggestions

I welcome any suggestions or improvements that could help optimize or expand this setup is welcome.

---

## 📁 Purpose of the Repository

This repository was created primarily for **backup purposes**. In case I need to recreate or restore any of the services, I can easily use the files from this repository. Most of the configuration is kept simple and modular using `.env` files, allowing quick adjustments if necessary.

---

## ⚙️ Pending

- NextCloud
- Improving security and backup processes.

---

## License

This project is open-source and available under the [MIT License](LICENSE).

