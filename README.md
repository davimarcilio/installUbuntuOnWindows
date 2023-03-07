## Passo 1 Comando para instalar WSL no Windows (PowerShell Admin):

- dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

## Passo 2 Comando para instalar WSL no Windows (PowerShell Admin):

- dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

## Passo 3

- REINICIE O COMPUTADOR

## Passo 4 (Download the Linux kernel update package):

- https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi

## Passo 5 Comando para instalar WSL no Windows (PowerShell Admin):

- wsl --set-default-version 2

## Passo 6

- Instalar UBUNTU na Microsoft Store

## Passo 7 Comandos para executar no Ubuntu

- sudo apt update -y

- sudo apt upgrade -y

## Passo 8 Comando para remover senha UBUNTU

- sudo nano /etc/sudoers
  - no final do arquivo digite `seu-username ALL=(ALL:ALL) NOPASSWD:ALL`

## Passo 9 Instalar FISH como terminal

- sudo apt-add-repository ppa:fish-shell/release-3
- sudo apt update
- sudo apt install fish
- chsh -s /usr/bin/fish

## Passo 10 Instalar Starship no FISH

- curl -sS https://starship.rs/install.sh | sh

```js
// ~/.config/fish/config.fish
if status is-interactive
# Commands to run in interactive sessions can go here
end

set SPACEFISH_PROMPT_ADD_NEWLINE false

starship init fish | source

# Aliases
# alias cat="bat --theme=$(defaults read -globalDomain AppleInterfaceStyle &> /dev/null && echo default || echo GitHub)"
```

## Passo 11 Instalar nvm(Node Version Manager)

- curl -sL https://git.io/fisher | source && fisher install jorgebucaran/fisher

- fisher install jorgebucaran/nvm.fish
