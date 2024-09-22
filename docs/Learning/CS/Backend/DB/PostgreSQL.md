# PostgreSQL

## Install

### Postgresql

[PostgreSQL: Linux downloads (Ubuntu)](https://www.postgresql.org/download/linux/ubuntu/)

```bash
apt install postgresql 
```

### pgAdmin

[Download](https://www.pgadmin.org/download/pgadmin-4-apt/)

#### Setup the Repository

```bash
# Install the public key for the repository (if not done previously):
curl -fsS https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo gpg --dearmor -o /usr/share/keyrings/packages-pgadmin-org.gpg

# Create the repository configuration file:
sudo sh -c 'echo "deb [signed-by=/usr/share/keyrings/packages-pgadmin-org.gpg] https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'
```

#### Install pgAdmin

```bash
# Install for both desktop and web modes:
sudo apt install pgadmin4

# Install for desktop mode only: for local development
sudo apt install pgadmin4-desktop

# Install for web mode only:  for remote server
sudo apt install pgadmin4-web 

# Configure the webserver, if you installed pgadmin4-web:
sudo /usr/pgadmin4/bin/setup-web.sh
```

## Start and End

start/stop app

```bash
sudo systemctl start/stop postgresql
```

start/stop as start up

```bash
sudo systemctl enable/disable postgresql
```
