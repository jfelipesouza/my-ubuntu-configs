# 🖋️ Minhas configurações do Ubuntu

Este repositório contém um script simples para instalar as fontes **Fira Code** e **JetBrains Mono** localmente no Ubuntu 24 (ou em qualquer distribuição baseada em Debian), além de uma configuração para o terminal ZSH, focada em produtividade nas atividades de programação.

A instalação utiliza os arquivos **ZIP** já presentes na pasta, sem necessidade de baixar nada da internet.

---
## Pre-requisitos
Para seguir com este tutorial, é necessário ter o **curl** e o **git** instalados.

Execute o comando abaixo no terminal para garantir que tudo esteja atualizado e instalado:


```bash
 sudo apt update && sudo apt upgrade -y && sudo apt install curl git
```

## Configurando o terminal
  - Instale o ZSH:
  ```bash
  sudo apt install zsh
  ```
  - Instale o Oh My Zsh:
  ```bash
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

  ```
  - Instale o tema desejado, nesse caso irei instalar o spaceship:
  ```bash
  git clone https://github.com/spaceship-prompt/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1
  ```
  Após o download usando o git execute no terminal: 
  ```bash
    ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
  ```
  - Reinicie o shell.
  Se nada mudar, reinicie o sistema:
  ```bash
  sudo reboot
  ```
  - Copie o conteúdo do arquivo my-zshrc.txt para o seu .zshrc.

  O arquivo .zshrc pode estar oculto no gerenciador de arquivos — pressione Ctrl + H para exibir arquivos ocultos.
  Ou abra diretamente pelo terminal usando um editor de texto:
  ```
  code ~/.zshrc
  ```
  ### Adicionando Plugins

  Navegue no seu terminal para o diretorio **~/.oh-my-zsh/custom/plugins**.

  ```
  cd ~/.oh-my-zsh/custom/plugins
  ```
  
  Dentro do diretorio rode o comando abaixo para clonar os plugins necessarios:
  ``` 
  git clone https://github.com/zsh-users/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-history-substring-search
git clone https://github.com/zdharma-continuum/fast-syntax-highlighting
  ``` 

  Recarregue o arquivo de shell

  ``` 
  source ~/.zshrc
  ```
## 🚀 Instalando as fontes

Siga os passos abaixo para instalar as fontes no seu usuário local:

### 1️⃣ Verifique os arquivos

Certifique-se de que a pasta contém:

```
Fira_Code_v6.2.zip
JetBrainsMono-2.304.zip
install.sh
```

---

### 2️⃣ Dê permissão de execução ao script

```bash
chmod +x install.sh
```

---

### 3️⃣ Execute o instalador

```bash
./install.sh
```

O script irá:

* Criar a pasta `~/.local/share/fonts` se não existir
* Extrair os arquivos ZIP
* Copiar as fontes `.ttf` para a pasta de fontes
* Atualizar o cache de fontes do sistema

---

## 🖍️ Fontes Instaladas

* **Fira Code** (com ligatures)
* **JetBrains Mono** (com ligatures)

Após a instalação, as fontes estarão disponíveis em qualquer aplicativo (VS Code, terminal, editores de texto, etc).

---

## 💬 Informações

🛠️ **Autor:** João Felipe de Oliveira Souza
📅 **Versão:** 2.0 (Local Edition)
📄 **Licença:** MIT
