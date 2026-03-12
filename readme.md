## Como executar o palybook:
```bash
ansible-playbook playbook.yml -k
```

### Rodar nos hosts remotos
```bash
ansible-playbook playbook.yml --limit dev-desktop
```

### Rodar no host local
```bash
ansible-playbook playbook.yml --limit localhost
```

### Comando que estava utilizando para rodar remotamente no notebook com ubuntu 26.04
```
ansible-playbook playbook.yml --limit dev-desktop -k -K
```