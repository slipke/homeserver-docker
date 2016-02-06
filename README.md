# homeserver-docker
Setup a homeserver docker-environment using ansible, docker, rancher

## Install needed roles

`ansible-galaxy install -r install_roles.yml -p roles/`

## Homeserver

* Setup alltogether: `ansible-playbook init.yml -i inventory/ --ask-sudo-pass`

* Setup rancher (rancher.yml): `ansible-playbook rancher.yml -i inventory/ --ask-sudo-pass`
* Register nodes (register_nodes.yml): `ansible-playbook register_nodes.yml -i inventory/ --ask-sudo-pass`