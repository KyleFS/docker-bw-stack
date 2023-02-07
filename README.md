# Vaultwarden

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
