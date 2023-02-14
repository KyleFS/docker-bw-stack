# Vaultwarden

**The fail2ban setup assumes a Debian 10 environment. Adjustments need to be made for other platforms**

## Initial Setup

Clone this project and enter the directory.
```
mkdir /opt/bitwarden
cd /opt/bitwarden
git clone https://github.com/KyleFS/docker-bw-stack
```

Fill in the environmental variable file.
```
mv .env.sample .env
nano .env
```

Create an empty log file on the host file system
```
sudo touch /var/log/vaultwarden.log
```

The following commands will use the create a systemd service for easy management.
```
sudo systemctl link /opt/bitwarden/docker-bw-stack/docker.bitwarden.service
sudo systemctl enable docker.bitwarden.service
```

As a service, general commands can be used for management.
```
sudo service docker.status stop
sudo service docker.status start
sudo service docker.status restart
sudo service docker.status status
```
