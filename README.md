# Quick Start
localhost
```bash
$ cd ansible
$ ansible-playbook packages.yml --ask-become-pass
```

mint01
```bash
$ cd ansible
$ ansible-playbook --key-file ~/.ssh/_id wget.yml -i myinv -kK
```
# Packer Installation
```bash
$ curl -sS https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/packer.gpg

$ echo "deb [arch=amd64 signed-by=/usr/share/keyrings/packer.gpg] https://apt.releases.hashicorp.com bullseye main" | sudo tee /etc/apt/sources.list.d/packer.list

$ sudo apt-get update

$ sudo apt-get install packer
```
# Common Packages
Configure ```packages.yml```:
``` yml
---
-
  name: Install common packages
  hosts: localhost

  roles:
    - packer
    - docker
    - helm
    - kubic
    - cri-o
```
Build the playbook with:
``` bash
$ ansible-playbook  packages.yml --ask-become-pass
```
