# Ansible Lab (Based into Debian 13)
My personal ansible script to configure my personal server.

# Command to run ansible
`ansible-playbook playbooks/main.yml -i inventory/hosts.yml --user=root --ask-vault-pass`

# Tips
1. Install SSH-PASS.

2. Update your id_rsa permissions

`chmod 600 ~/.ssh/id_rsa` (PRIVATE)
`ssh-add ~/.ssh/id_rsa`

3. Edit vault.yml and encript

(Vault Content Example)

```
ssh_path: "PATH_TO_SSH_PUBLIC_KEY"
```

(Cript Command)

`ansible-vault encrypt inventory/group_vars/server/vault.yml` 

4. Edit nginx.yml and encript

(Nginx Content Example)

```
syncthing_domain: DNS_IP
domain_name: DOMAIN_NAME
email_cert: EMAIL
```

(Cript Command)

`ansible-vault encrypt inventory/group_vars/server/nginx.yml` 

5. Edit hosts.yml and encript

(Hosts Content Example)

```
server:
  hosts:
    SERVER_IP
```

(Cript Command)

`ansible-vault encrypt inventory/hosts.yml` 

6. Edit s3.yml and encript

(S3 Content Example)

```
bucket_name: "BUCKET-NAME"
```

(Cript Command)

`ansible-vault encrypt inventory/group_vars/server/s3.yml` 

7. Edit awd.yml and encript

(AWS Content Example)

```
aws_access_key_id: ACCESS_KEY
aws_secret_access_key: SECRET_KEY
aws_region: us-east-1
```

(Cript Command)

`ansible-vault encrypt inventory/group_vars/server/aws.yml` 