# Self-Hosted IAM & Zero Trust Lab

## Objective
Designed and deployed a centralized Identity and Access Management (IAM) environment to enforce Role-Based Access Control (RBAC), Single Sign-On (SSO), and Multi-Factor Authentication (MFA) across internal applications. This lab simulates an enterprise environment by integrating a self-hosted Identity Provider (IdP) with a third-party application.

## Technologies Used
- **Hypervisor:** Proxmox VE (Bare-metal)
- **Compute:** Debian 13 (LXC Containers)
- **Containerization:** Docker & Docker Compose
- **Identity Provider (IdP):** Authentik
- **Service Provider (SP):** Portainer
- **Protocols:** OIDC (OpenID Connect), OAuth2
- **Networking:** iptables (NAT), Split-Horizon Routing

## Project Documentation
Click the links below to see implementation steps and screenshots for each feature:
- [Role-Based Access Control (RBAC)](./doc/RBAC.md)
- [Multi-Factor Authentication (MFA)](./doc/MFA.md)
- [Single Sign-On (SSO) Integration](./doc/SSO.md)

## Architecture & Networking
- **Host Networking:** The Proxmox host operates over Wi-Fi. A custom NAT (Network Address Translation) bridge was configured using `iptables` to route traffic from isolated container subnets (`10.10.10.0/24`) out to the physical network.
- **Split-Horizon Routing:** Configured distinct URLs for front-channel (browser-to-server) and back-channel (server-to-server) communication. External IPs were used for browser redirects, while internal container IPs were used for API token exchanges to prevent routing loops.
- **IdP (Authentik):** `10.10.10.101`
- **SP (Portainer):** `10.10.10.102`
