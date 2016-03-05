# Codingstones Operations Repository

This repository will contain ansible playbooks for codingstones and other
automations

## Keys special directory and vault password

This directory will contain private keys and should not be uploaded to Git
server.

Please, ask for a copy privately.

## Examples


### Run ansible on all hosts

```
ansible-playbook site.yml -sK --vault-password-file=.vault-password
```
