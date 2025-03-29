INSTALL SSH-PASS

`chmod 600 ~/.ssh/id_rsa` (PRIVATE)
`ssh-add ~/.ssh/id_rsa`

`ansible-playbook playbooks/main.yml -i inventory/hosts.yml --user=root --ask-pass`



# Script to install syncthing
Tip: Seems running the script below with ansible not working correctly, please run manually the commands bellow!

```
systemctl start syncthing@syncthing.service --now
sed -i 's/127\.0\.0\.1:8384/SERVER_IP:8384/' /home/syncthing/.local/state/syncthing/config.xml
systemctl restart syncthing@syncthing.service 
```
