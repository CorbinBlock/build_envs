pipeline {
    agent none
    stages {
         stage('UNIX-02-FEDORA') {
            agent {
                label 'UNIX-02-FEDORA'
            }
            steps {
                sh"""
                # dnf update -y
                # yum update -y
                # systemctl enable --now cockpit.socket
                # dnf install git -y
                
                # echo "export GIT_EMAIL='williamcorbinblock@gmail.com'" > /etc/profile.d/git_email.sh
                # echo "export GIT_USERNAME='CorbinBlock'" > /etc/profile.d/git_username.sh
                # git config --global user.name \$GIT_USERNAME
                # git config --global user.name
                # git config --global user.email \$GIT_EMAIL
                # git config --global user.email
                # dnf install vim -y
                # dnf remove buildah skopeo podman containers-common atomic-registries docker container-tools -y
                # rm -rf /etc/containers/* /var/lib/containers/* /etc/docker /etc/subuid* /etc/subgid*
                # cd ~ && rm -rf /.local/share/containers/
                # dnf remove podman.x86_64 -y
                # dnf autoremove -y
                # dnf -y install dnf-plugins-core -y
                # dnf config-manager --add-repo=https://download.docker.com/linux/fedora/docker-ce.repo
                # dnf repolist -v
                # dnf install docker-ce docker-ce-cli containerd.io -y
                # systemctl enable --now docker
                # systemctl is-active docker
                # curl -L "https://github.com/docker/compose/releases/download/1.23.2/docker-compose-\$(uname -s)-\$(uname -m)" -o docker-compose
                # mv docker-compose /usr/local/bin && chmod +x /usr/local/bin/docker-compose
                # ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
                # dnf group install "Development Tools" -y
                # dnf history userinstalled
                mkdir -p /git
                cd /git
                ls -ltr
                git clone https://github.com/CorbinBlock/bash.git || (cd /git/bash ; git pull --no-rebase)
                git clone https://github.com/CorbinBlock/docker.git || (cd /git/docker ; git pull --no-rebase)
                git clone https://github.com/CorbinBlock/jenkins.git || (cd /git/jenkins ; git pull --no-rebase)
                git clone https://github.com/CorbinBlock/python.git || (cd /git/python ; git pull --no-rebase)
                
                
                # cd /git/docker/jenkins_container
                # sh create_network.sh
                # docker network inspect jenkins >/dev/null 2>&1 ||
                # docker network create jenkins
                # sh build_container.sh
                # sh run_container.sh
                # docker container ls --no-trunc | grep jenkins
                # sh print_jenkins_admin_password.sh <instance_id>
                
                # ssh-keygen -f ~/.ssh/jenkins_agent_key
                # useradd -d /var/lib/jenkins jenkins
                
                # docker container rm debian_dev_env -f
                # docker builder prune -a -f
                # docker system prune --all --force --volumes
                # cd /git/docker/debian_dev_env
                # docker build -t debian_dev_env . # --no-cache=true
                # docker run -d -p 5000:5000 -t --name debian_dev_env debian_dev_env
                # docker save debian_dev_env | gzip > /tmp/debian_dev_env.tar.gz
                
                # cd /tmp
                # aws s3 cp debian_dev_env.tar.gz s3://s3-bucket-cblock
                
                """
            }
        }
        stage('WIN-02-ASUS') {
            agent {
                label 'WIN-02-ASUS'
            }
            steps {
                pwsh("""
                # dbeaver - must install manually to accept prompt
                # winget install 9PNKDR50694P -h #dbeaver
                # winget install AdoptOpenJDK.OpenJDK.11 -h
                # winget install Apple.iTunes -h
                # winget install Adobe.Acrobat.Reader.64-bit -h
                # winget install Amazon.AWSCLI -h
                # winget install Cockos.Reaper -h
                # winget install Docker.DockerDesktop -h
                # winget install DominikReichl.KeePass -h
                # winget install Fedora.FedoraMediaWriter -h
                # winget install Git.Git -h
                # winget install Google.Chrome -h
                # winget uninstall 'Azure Data Studio' -h
                # winget install Microsoft.SQLServerManagementStudio -h
                # winget install Microsoft.VisualStudioCode -h
                # winget install Notepad++.Notepad++ -h
                # winget install Python.Python.3 -h
                # winget install RaspberryPiFoundation.RaspberryPiImager -h
                # winget install TheGroovyTeam.Groovy -h
                # winget install Valve.Steam -h
                # winget install WinDirStat -h
                # Get-NetIPAddress | Format-Table
                # Install-Module -Force Microsoft.PowerShell.SecretManagement
                # Install-Module -Force Microsoft.PowerShell.SecretStore
                # Install-Module -Force -Name SecretManagement.KeePass -RequiredVersion 0.9.2
                New-Item -ItemType Directory -Force -Path /git/docker
                New-Item -ItemType Directory -Force -Path /git/jenkins
                New-Item -ItemType Directory -Force -Path /git/powershell
                New-Item -ItemType Directory -Force -Path /git/python
                cd /git
                git clone https://github.com/CorbinBlock/docker.git || (cd /git/docker && git pull --no-rebase)
                git clone https://github.com/CorbinBlock/jenkins.git || (cd /git/jenkins && git pull --no-rebase)
                git clone https://github.com/CorbinBlock/powershell.git || (cd /git/powershell && git pull --no-rebase)
                git clone https://github.com/CorbinBlock/python.git || (cd /git/python && git pull --no-rebase)
                
                cd /git/powershell_internal/util_powershell
                
                # pscp.exe -pw \$env:FEDORA root@devenvrhel.ddns.net:/tmp/debian_dev_env.tar.gz /wslsources
                
                # Get-ChildItem /wslsources
            
                # "/Program Files/Docker/Docker/Docker Desktop.exe"            
                # cd /wslsources
                # docker container rm debian_dev_env -f
                # docker builder prune -a -f
                # docker system prune --all --force --volumes
                # docker load --input debian_dev_env.tar.gz
                # docker run -d -p 5000:5000 -t --name debian_dev_env debian_dev_env
                
                # dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
                # dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
                # Invoke-WebRequest -Uri "https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi" -Outfile /tmp/wsl_update_x64.msi
                # msiexec.exe /I /tmp/wsl_update_x64.msi /quiet 
                # wsl --set-default-version 2
                # wsl --unregister debian_dev_env
                # wsl --import debian_dev_env /wslsources/debian_dev_env /wslsources/debian-11-generic-amd64-daily.tar.xz
                
                wsl --list
                # wsl --unregister Debian
                # winget uninstall TheDebianProject.DebianGNULinux_76v4gfsz19hv4 -h
                # winget install Debian.debian -h
                # start-process debian
                
                # bash -c 'rm -f /etc/wsl.conf'
                # bash -c 'echo "[user]" >> /etc/wsl.conf'
                # bash -c 'echo "default=root" >> /etc/wsl.conf'
                # wsl --shutdown
                # wsl --set-default Debian
                # wsl --list
                # bash -c "apt-get update && apt-get upgrade -y; apt-get install vim git git-lfs python3 python3-pip python3-venv openjdk-11-jdk curl -y"
                """)
            }
        }
        stage('UNIX-01-DEBIAN') {
            agent {
                label 'UNIX-01-DEBIAN'
            }
            steps {
                sh"""
                ls -ltr;id;hostname
                # apt-get update -y && apt-get upgrade -y
                # apt-get install sudo
                # apt-get install vim -y
                # apt-get install openjdk-11-jdk -y
                # passwd
                # useradd -m -s /bin/bash cblock
                # passwd cblock
                # mkdir /jenkins
                # chown -R cblock /jenkins
                # sudo echo 'export GIT_USERNAME=<username>' >> /etc/profile.d/git_username.sh
                # sudo echo 'export GIT_EMAIL=<email>' >> /etc/profile.d/git_email.sh
                # sudo apt-get update && sudo apt-get upgrade -y
                # sudo apt-get install git -y
                # git --version
                # git config --global user.name \$GIT_USERNAME
                # git config --global user.name
                # git config --global user.email \$GIT_EMAIL
                # git config --global user.email
                # sudo apt-get install python3 python3-pip python3-venv -y
                # python3 --version
                # sudo apt-get remove docker docker-engine docker.io containerd runc
                # sudo apt-get update
                # sudo apt-get install \
                #    ca-certificates \
                #    curl \
                #    gnupg \
                #    lsb-release
                # curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
                # echo "deb [arch=\$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian \$(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
                # sudo apt-get update
                # sudo apt-get install docker-ce docker-ce-cli containerd.io
                # sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-\$(uname -s)-\$(uname -m)" -o /usr/local/bin/docker-compose
                # sudo chmod +x /usr/local/bin/docker-compose
                # docker-compose --version
                # vim /etc/ssh/sshd_config
                # Edit line to the following: PermitRootLogin yes
                # Restart SSH server
                # /etc/init.d/ssh restart
                mkdir -p /git
                cd /git
                git clone https://github.com/CorbinBlock/bash.git || (cd /git/bash ; git pull --no-rebase)
                git clone https://github.com/CorbinBlock/docker.git || (cd /git/docker ; git pull --no-rebase)
                git clone https://github.com/CorbinBlock/jenkins.git || (cd /git/jenkins ; git pull --no-rebase)
                git clone https://github.com/CorbinBlock/python.git || (cd /git/python ; git pull --no-rebase)
                
                cd /tmp
                # docker container rm debian_dev_env -f
                # docker volume prune -f
                # docker builder prune -a -f
                # docker load --input debian_dev_env.tar.gz
                # docker run -d -p 5000:5000 -t --name debian_dev_env debian_dev_env
                
                """
            }
        }
    }
}
