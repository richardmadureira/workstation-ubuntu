# Instruções

Este projeto instala bilbiotecas e aplicativos para o perfil de desenvolvedores.
Após a instalação do `Ubuntu 26.04`, é necessário instalar o ssh para permitir conexões remotas realizadas pelo ansible. O comando de instalação é:
```bash
sudo apt update && sudo apt install ssh -y
```

## Observação
Como o Ubuntu `26.04` possui um novo aplicativo sudo (o sudo-rs, feito em rust), só consegui fazer funcionar com a inclusão do usuário na lista de sudoers assim:
* Executar o comando `sudo visudo`
* adicionar, ao final do arquivo, a seguinte linha: `richard ALL=(ALL) NOPASSWD: ALL`

O comando anterior irá fazer com que não seja solicitado a senha de root para o usuário `richard`.

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