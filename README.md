# Ansible Lab
My personal ansible script to configure my personal server.

# Tips
1. Install SSH-PASS.
2. Update your id_rsa permissions

`chmod 600 ~/.ssh/id_rsa` (PRIVATE)
`ssh-add ~/.ssh/id_rsa`

3. Run the command bellow to run the ansible script. 
**DON'T FORGET CHANGE SERVER IP INTO hosts.yml**

`ansible-playbook playbooks/main.yml -i inventory/hosts.yml --user=root`
