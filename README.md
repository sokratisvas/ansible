# Install Ansible Galaxy Role with:
```bash
$ ansible-galaxy install -r requirements.yml
```

# Configure ```packages.yml```:
``` yml
---
-
  name: Install common packages
  hosts: localhost

  roles:
    - docker
    - cri-o
    - packer
    - helm
```

# Run the playbook with:
``` bash
$ ansible-playbook packages.yml --ask-become-pass
```


