### Service Provider Integration (Portainer)
- Deployed Portainer (a Docker management UI) in a separate LXC container.
- Configured Portainer to trust Authentik as its OIDC provider.
- Mapped the `email` claim as the User Identifier to ensure seamless automatic provisioning.
- Enabled automatic user provisioning so users logging in via SSO are automatically granted access without manual admin creation.

<img width="1748" height="817" alt="Screenshot_20261102_102254" src="https://github.com/user-attachments/assets/d3b68e9d-9d06-4d57-b726-9812a8c35283" />
<img width="1920" height="876" alt="Screenshot_20261102_102717" src="https://github.com/user-attachments/assets/ec946659-d862-454d-8f40-8fb9d5bbc17e" />
<img width="1920" height="886" alt="Screenshot_20261102_102905" src="https://github.com/user-attachments/assets/6d4f67a9-13b5-4ffa-b941-8181998261b6" />
<img width="1920" height="884" alt="Screenshot_20261102_110326" src="https://github.com/user-attachments/assets/e2948c6f-57a7-4d63-b2ac-91639ff4ac25" />
<img width="1920" height="884" alt="Screenshot_20261102_110357" src="https://github.com/user-attachments/assets/0dc39321-775d-4204-9312-92b84fa87452" />
<img width="1920" height="886" alt="Screenshot_20261102_110437" src="https://github.com/user-attachments/assets/b87da847-3e05-4bf1-999b-fc700a0472c3" />
<img width="1920" height="891" alt="Screenshot_20261102_234906" src="https://github.com/user-attachments/assets/4bead769-fb9a-49c9-a82d-31e38ee47db3" />
<img width="1920" height="884" alt="Screenshot_20261102_234923" src="https://github.com/user-attachments/assets/a065126f-6509-4a07-9d82-1b391aa1ce65" />
<img width="1920" height="876" alt="Screenshot_20261103_000354" src="https://github.com/user-attachments/assets/e3ed3a41-0152-4f21-9776-ef989fe01d80" />
<img width="1920" height="882" alt="Screenshot_20261103_000407" src="https://github.com/user-attachments/assets/18438501-1240-4b93-b8be-b672e1d5493a" />
<img width="1920" height="882" alt="Screenshot_20261103_000418" src="https://github.com/user-attachments/assets/2df90e64-984d-42df-ab69-9417fe518172" />
<img width="1920" height="887" alt="Screenshot_20261103_004832" src="https://github.com/user-attachments/assets/06cc493a-14df-4f02-bf64-d15a44838a0d" />

