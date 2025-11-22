# Ansible Lab
My personal ansible script to configure my personal server.

# Command to run ansible
`ansible-playbook playbooks/main.yml -i inventory/hosts.yml --user=root --ask-vault-pass`

# Tips
1. Install SSH-PASS.
2. Update your id_rsa permissions

`chmod 600 ~/.ssh/id_rsa` (PRIVATE)
`ssh-add ~/.ssh/id_rsa`

3. Edit vault.yml and encript

`ssh_path: "PATH_TO_SSH_PUBLIC_KEY"` (Vault Content Example)
`ansible-vault encrypt inventory/group_vars/server/vault.yml` (Cript Command)

4. Edit nginx.yml and encript

`syncthing_domain: DNS_OR_IP` (Nginx Content Example)
`ansible-vault encrypt inventory/group_vars/server/nginx.yml` (Cript Command)

5. Edit hosts.yml and encript

(Hosts Content Example)
```
server:
  hosts:
    SERVER_IP
```
`ansible-vault encrypt inventory/hosts.yml` (Cript Command)