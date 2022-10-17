# Configure ```packages.yml```:
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

# Build the playbook with:
``` bash
$ ansible-playbook packages.yml --ask-become-pass
```

# Install Ansible Galaxy Role with:
```bash
$ ansible-galaxy install -r requirements.yml
```

