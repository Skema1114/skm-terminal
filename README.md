# skm-terminal

Modificar as politicas do powershell para executar scripts
```sh
Set-ExecutionPolicy RemoteSigned
```

Instalar os modulos posh-git e oh-my-posh
```sh
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser
```

Importar os módulos e escolher o tema (os mesmos podem ser encontrados em `C:\Users\[nome usuário]\Documents\WindowsPowerShell\Modules\oh-my-posh\[versão]\themes`)
```sh
Import-Module posh-git
Import-Module oh-my-posh
Set-PoshPrompt -Theme Honukai
```

(opcional) Instalar o chocolatey
```sh
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

(opcional) Instalar a fonte Fira Code com o chocolatey (OBS: A Fira Code precisa ser instalada, opcional é so a forma de fazer isso)
```sh
choco install firacode-ttf
```
