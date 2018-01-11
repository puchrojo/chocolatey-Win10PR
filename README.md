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
    choco install kindle --version 1.17
    
## Install the Packages.config
    cinst Win102017-Choco.config
    
## Update all packages
    choco upgrade all -y
    choco upgrade all --except="'kindle'"

Es sollte auch mit pin gehen, kriege ich aber nicht:
https://superuser.com/questions/972178/how-to-update-all-chocolatey-packages-except-one




{% capture docker_ubuntu %}

Install Docker from Ubuntu's repositories:

```bash
apt-get update
apt-get install -y docker.io
```

or install Docker CE 17.03 from Docker's repositories for Ubuntu or Debian:

```bash
apt-get update && apt-get install -y curl apt-transport-https
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add -
cat <<EOF >/etc/apt/sources.list.d/docker.list
deb https://download.docker.com/linux/$(lsb_release -si | tr '[:upper:]' '[:lower:]') $(lsb_release -cs) stable
EOF
apt-get update && apt-get install -y docker-ce=$(apt-cache madison docker-ce | grep 17.03 | head -1 | awk '{print $3}')
```

{% endcapture %}

{% capture docker_centos %}

Install Docker using your operating system's bundled package:

```bash
yum install -y docker
systemctl enable docker && systemctl start docker
```

{% endcapture %}

Test Formatirung

