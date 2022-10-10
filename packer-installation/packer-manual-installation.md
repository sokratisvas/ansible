# Proper manual installation
```bash
$ curl -sS https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/packer.gpg

$ echo "deb [arch=amd64 signed-by=/usr/share/keyrings/packer.gpg] https://apt.releases.hashicorp.com bullseye main" | sudo tee /etc/apt/sources.list.d/packer.list

$ sudo apt-get update

$ sudo apt-get install packer
```
