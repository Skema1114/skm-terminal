# skm-terminal

## Instalação
Modificar as politicas do powershell para executar scripts
```powershell
Set-ExecutionPolicy RemoteSigned
```

Instalar os modulos posh-git e oh-my-posh
```powershell
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser
```

Verifique se existe o arquivo $PROFILE, se não existir será criado
```powershell
if (!(Test-Path -Path $PROFILE )) { New-Item -Type File -Path $PROFILE -Force }
notepad $PROFILE

```

Importar os módulos e escolher o tema (os mesmos podem ser encontrados em `C:\Users\[nome usuário]\Documents\WindowsPowerShell\Modules\oh-my-posh\[versão]\themes`)
```powershell
Import-Module posh-git
Import-Module oh-my-posh
Set-PoshPrompt -Theme Paradox
```
`OBS: Caso a última linha apresente erros depois, pode trocar por:`
```powershell
Set-Theme Paradox
```

(opcional) Instalar o chocolatey
```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

(opcional) Instalar a fonte Fira Code com o chocolatey (OBS: A Fira Code precisa ser instalada, opcional é so a forma de fazer isso)
```sh
choco install firacode-ttf
```

## Referências
- https://github.com/JanDeDobbeleer/oh-my-posh2
- https://blog.rocketseat.com.br/terminal-com-oh-my-zsh-spaceship-dracula-e-mais/
- https://docs.microsoft.com/pt-br/windows/terminal/tutorials/powerline-setup (OBS: Não execute o `Install-Module -Name PSReadLine -Scope CurrentUser -Force -SkipPublisherCheck`)
- https://zimmergren.net/making-windows-terminal-look-awesome-with-oh-my-posh/
