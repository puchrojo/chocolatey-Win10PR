# chocolatey-Win10PR
My favorite Windows Software Chocolatey Config File. Nothing more.  
https://chocolatey.org/packages

## Install Chocolatey
Start PowerShell as admin:

    Set-ExecutionPolicy -ExecutionPolicy RemoteSigned
    iwr https://chocolatey.org/install.ps1 -UseBasicParsing | iex
    choco feature enable -n allowGlobalConfirmation
    
## Install individual packages
    choco install notepadplusplus.install
    choco install chocolateygui
    
## Install the Packages.config
    cinst Win102017-Choco.config
    
## Update all packages
    choco upgrade all -y
    choco upgrade all --except="'kindle'"

Es sollte auch mit pin gehen, kriege ich aber nicht:
https://superuser.com/questions/972178/how-to-update-all-chocolatey-packages-except-one


