# 🚀 Meu Ambiente de Desenvolvimento

![Banner](https://img.shields.io/badge/Developer%20Setup-Ambiente%20Pessoal-blue?style=for-the-badge&logo=ubuntu&logoColor=white)

Este repositório contém um checklist e comandos para configurar rapidamente meu ambiente de desenvolvimento em novas máquinas.

Foco principal: **Linux Ubuntu** 🐧 | Desenvolvimento de **Software** 💻 | Produtividade ⚡

---

# 📦 Pós-Instalação

> ⚡ Sempre priorizar instalações via terminal para agilidade e automação.

---

## 🛠️ Programas Essenciais

### 🧩 Visual Studio Code Insiders
```bash
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -o root -g root -m 644 packages.microsoft.gpg /etc/apt/trusted.gpg.d/
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/code-insiders stable main" > /etc/apt/sources.list.d/vscode-insiders.list'
sudo apt update
sudo apt install code-insiders
```

### 🔥 Insomnium (alternativa ao Postman)
```bash
wget https://github.com/Fluorohydride/Insomnium/releases/download/v1.10.0/insomnium_1.10.0_amd64.deb
sudo apt install ./insomnium_1.10.0_amd64.deb
```
> [Link para novas versões](https://github.com/Fluorohydride/Insomnium/releases)

### 🌐 Zen Browser
```bash
# Instalar Flatpak (caso ainda não tenha)
sudo apt install flatpak

# Adicionar Flathub (caso ainda não tenha)
sudo flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo

# Instalar Zen Browser
flatpak install flathub app.zen_browser.zen
```

### 🌍 Google Chrome
```bash
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt install ./google-chrome-stable_current_amd64.deb
```

### 🐳 Docker
```bash
sudo apt update
sudo apt install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

sudo mkdir -m 0755 -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] \
  https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# Adicionar usuário ao grupo docker
sudo usermod -aG docker $USER
newgrp docker
```

### 🎙️ Discord
```bash
wget -O discord.deb "https://discord.com/api/download?platform=linux&format=deb"
sudo apt install ./discord.deb
```

### 🧠 Obsidian
```bash
wget https://github.com/obsidianmd/obsidian-releases/releases/download/v1.5.3/obsidian_1.5.3_amd64.deb
sudo apt install ./obsidian_1.5.3_amd64.deb
```
> [Link para novas versões](https://github.com/obsidianmd/obsidian-releases/releases)

### 🤖 Cursor (Editor de Código com IA)
- Baixar manualmente: [cursor.sh](https://cursor.sh/)

---

## ⚙️ Ferramentas de Desenvolvimento

### ☁️ AWS CLI
```bash
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```

### 🛠️ Makefile (pacote make)
```bash
sudo apt update
sudo apt install build-essential
```

---

## 💻 Linguagens de Programação

### 🦫 Go
```bash
sudo apt update
sudo apt install golang-go
```
> Ou instalar manualmente a versão mais recente:
```bash
wget https://go.dev/dl/go1.22.2.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.22.2.linux-amd64.tar.gz
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.bashrc
source ~/.bashrc
```

### 🌐 Node.js, npm e nvm (para TypeScript)
```bash
# Instalar NVM
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source ~/.bashrc

# Instalar Node LTS
nvm install --lts
nvm use --lts
npm -v
```

### 🐘 PHP
```bash
sudo apt update
sudo apt install php php-cli php-mbstring php-xml php-curl php-zip php-mysql
```

---

# ✅ Checklist Pós-Instalação

- [ ] Configurar SSH para GitHub
- [ ] Instalar extensões do VSCode
- [ ] Configurar Docker para rodar sem sudo
- [ ] Clonar repositórios principais
- [ ] Configurar aliases no terminal
- [ ] Ajustar temas, ícones e fontes

---

# 📚 Links Úteis
- [Zen Browser](https://zen-browser.app/)
- [Docker Documentation](https://docs.docker.com/)
- [Obsidian MD](https://obsidian.md/)
- [Cursor IDE](https://cursor.sh/)

---
