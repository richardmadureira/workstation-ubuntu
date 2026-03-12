## Como executar o palybook:
```bash
ansible-playbook playbook.yml -k
```

### Rodar nos hosts remotos
```bash
ansible-playbook playbook.yml --limit dev-desktop -k
```

### Rodar no host local
```bash
ansible-playbook playbook.yml --limit localhost -k
```