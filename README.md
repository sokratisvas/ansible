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
