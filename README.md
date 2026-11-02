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

## 🔐 Implementation Details
1. **User Provisioning:** Created local users and administrative accounts within Authentik.
2. **Role-Based Access Control (RBAC):** Created an "Engineering" group. Assigned specific users to this group to manage access rights.
3. **SSO Application Configuration:** Configured an OIDC (OpenID Connect) provider for a test application.
4. **Authorization Policies:** Bound the application to the "Engineering" group. Verified that users outside the group could authenticate but were not authorized to see the application, successfully enforcing the Principle of Least Privilege.

## 📸 Screenshots
*(Add your screenshots here: Authentik dashboard, User group assignment, App bindings, User dashboard showing the app)*

<img width="1920" height="886" alt="Screenshot_20261031_200327" src="https://github.com/user-attachments/assets/e5628089-4116-4b71-8fc5-cf970098f139" />
<img width="1920" height="896" alt="Screenshot_20261101_201031" src="https://github.com/user-attachments/assets/af5e8ab3-7d15-4328-8aff-5f25f2356652" />

