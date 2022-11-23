```sh
p11tool --list-tokens
sudo ln -s /usr/lib/libaetpkss.so opensc-pkcs11.so
modutil -dbdir sql:.pki/nssdb/ -add "Star Sign GD" -libfile /usr/lib/libaetpkss.so
curl https://safesign.gdamericadosul.com.br/content/SafeSign_IC_Standard_Linux_ub2204_3.8.0.0_AET.000.zip
```

## Instalação do drive (SafeSign)
```sh
curl -o safesign.zip https://safesign.gdamericadosul.com.br/content/SafeSign_IC_Standard_Linux_ub2204_3.8.0.0_AET.000.zip
unzip safesign.zip /tmp
sudo dpkg -i /tmp/"SafeSign IC Standard Linux 3.8.0.0-AET.000 ub2204 x86_64".deb
```
## instalação das bibliotecas e utilitários necessários
```sh
echo "deb http://security.ubuntu.com/ubuntu focal-security main" | sudo tee /etc/apt/sources.list.d/focal-security.list
sudo apt update
sudo apt install libssl1.1
```