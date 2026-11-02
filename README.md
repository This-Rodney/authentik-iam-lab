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
<img width="1920" height="886" alt="Screenshot_20261031_200327" src="https://github.com/user-attachments/assets/e5628089-4116-4b71-8fc5-cf970098f139" />
<img width="1920" height="896" alt="Screenshot_20261101_201031" src="https://github.com/user-attachments/assets/af5e8ab3-7d15-4328-8aff-5f25f2356652" />
<img width="1920" height="896" alt="Screenshot_20261101_202834" src="https://github.com/user-attachments/assets/3a4d9c03-c41c-415c-ba03-83d60c2f7c8c" />
<img width="1920" height="885" alt="Screenshot_20261101_202905" src="https://github.com/user-attachments/assets/f2d52dd0-43d2-4552-9b1b-10dd0f565bf2" />
<img width="1920" height="886" alt="Screenshot_20261101_203402" src="https://github.com/user-attachments/assets/80926971-4ff4-4c58-ad62-8883b8469a59" />
<img width="1920" height="885" alt="Screenshot_20261101_204407" src="https://github.com/user-attachments/assets/0cb37504-e464-4d78-9868-187aa2e4da79" />
<img width="1873" height="885" alt="Screenshot_20261101_210636" src="https://github.com/user-attachments/assets/5a030122-a918-4cad-82fd-d04c24f43d5e" />
<img width="1873" height="885" alt="Screenshot_20261101_210712" src="https://github.com/user-attachments/assets/dd3b49fc-a099-4428-a941-53b83f7a7b34" />
<img width="1873" height="973" alt="Screenshot_20261101_210850" src="https://github.com/user-attachments/assets/bafcdb2d-ec62-48da-98a1-056ee37783d3" />








