# Repositório APT Não-Oficial oxipng
Repositório APT Não-Oficial do [oxipng](https://github.com/shssoichiro/oxipng).

Use este repositório para instalar e atualizar o pacote oxipng com facilidade usando o APT.

Antes de confiar neste repositório, verifique a integridade dos arquivos e considere sua segurança primeiro. Crie seu próprio repositório APT usando este como base ou utilize o meu que buscará atualizações diariamente.

# Requisitos

* Debian/Ubunto ou qualquer distro derivado destes.

# Como instalar o repositório APT
Para que o APT identifique este repositório e seja capaz de instalar e atualizar o Discord você deve executar os códigos abaixo.
```shell
sudo apt remove oxipng # Apenas se você instalou o oxipng usando o arquivo deb. Neste caso, desinstale primeiro.
wget -qO- https://maeglithier.github.io/oxipng-apt/pubkey.asc | sudo gpg --dearmor -o /usr/share/keyrings/oxipng-archive-keyring.gpg
echo "deb [arch=amd64,arm64 signed-by=/usr/share/keyrings/oxipng-archive-keyring.gpg] https://maeglithier.github.io/oxipng-apt stable main" | sudo tee /etc/apt/sources.list.d/oxipng.list >/dev/null
sudo apt update
sudo apt install oxipng -y # Agora você está pronto para instalar e atualizar sempre que uma nova versão lançar.
```

# Como faço para desinstalar este repositório?
Para remover este repositório e sua chave pública você deve executar os códigos abaixo.
```shell
sudo apt remove oxipng # Apenas se você ainda não desinstalou o oxipng. Neste caso, desinstale primeiro.
sudo rm /usr/share/keyrings/oxipng-archive-keyring.gpg
sudo rm /etc/apt/sources.list.d/oxipng.list
```

# Checksum

12cdffc13c4fe5c80d954e7280c86679202ac4a70ae98662210519c571ff088f  pool/main/o/oxipng/oxipng_9.1.2-1_amd64.deb

1881edf3c0fe321cf552ef27cc7dfeff45b782b090e93688ef0cec703da3718e  pool/main/o/oxipng/oxipng_9.1.2-1_arm64.deb

# Copyright
O instalador do oxipng (arquivos deb) são distribuidos sob a licença MIT.