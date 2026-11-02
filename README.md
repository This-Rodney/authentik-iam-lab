# Self-Hosted Identity & Access Management (IAM) Lab

## 🎯 Objective
Deployed a self-hosted Identity Provider (IdP) to centralize authentication and implement Role-Based Access Control (RBAC) for internal applications.

## 🧰 Technologies Used
- Proxmox VE (Bare-metal hypervisor)
- Debian 13 (LXC Container)
- Docker & Docker Compose
- Authentik (Open-Source IdP)

## 🏗️ Architecture
- Proxmox host runs on Wi-Fi, utilizing iptables NAT to route container traffic.
- Authentik runs in a Docker container at `10.10.10.101`.
- Port forwarding configured on the host to allow secure external access.

## 🔐 Implementation Details
1. **User Provisioning:** Created local users and administrative accounts within Authentik.
2. **Role-Based Access Control (RBAC):** Created an "Engineering" group. Assigned specific users to this group to manage access rights.
3. **SSO Application Configuration:** Configured an OIDC (OpenID Connect) provider for a test application.
4. **Authorization Policies:** Bound the application to the "Engineering" group. Verified that users outside the group could authenticate but were not authorized to see the application, successfully enforcing the Principle of Least Privilege.

## 📸 Screenshots
*(Add your screenshots here: Authentik dashboard, User group assignment, App bindings, User dashboard showing the app)*