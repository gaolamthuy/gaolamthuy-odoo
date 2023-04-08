## Local development environments

```bash
sudo docker-compose -f ~/gaolamthuy-odoo16/docker-compose.dev.yml -p "odoo-gaolamthuy-dev" up --build --force-recreate -d
```

```bash
sudo docker-compose -f ~/gaolamthuy-odoo16/docker-compose.dev.yml -p "odoo-gaolamthuy-dev" down
```

```bash
sudo mkdir -p ~/gaolamthuy-odoo16/postgresql && 
sudo mkdir -p ~/gaolamthuy-odoo16/etc &&
sudo mkdir -p ~/gaolamthuy-odoo16/addons &&
sudo chmod -R 777 ~/gaolamthuy-odoo16/postgresql &&
sudo chmod -R 777 ~/gaolamthuy-odoo16/etc && 
sudo chmod -R 777 ~/gaolamthuy-odoo16/addons
```

Hard reset stack

```bash
sudo rm -rf ~/gaolamthuy-odoo16/etc/addons
sudo rm -rf ~/gaolamthuy-odoo16/etc/filestore
sudo rm -rf ~/gaolamthuy-odoo16/etc/sessions
sudo rm -rf ~/gaolamthuy-odoo16/etc/odoo-server.log
sudo rm -rf ~/gaolamthuy-odoo16/postgresql
```


## Staging environments

First time setup
```bash
sudo git clone -b staging https://github.com/gaolamthuy/gaolamthuy-odoo16.git
```

```bash
sudo nano ~/gaolamthuy-odoo16/.env
```

*Add stack to caddy network*

CD
```bash
sudo git pull
```

```bash
sudo docker-compose -f ~/gaolamthuy-odoo16/docker-compose.stage.yml -p "odoo-gaolamthuy-stage" up --build --force-recreate -d
```

```bash
sudo docker-compose -f ~/gaolamthuy-odoo16/docker-compose.stage.yml -p "odoo-gaolamthuy-stage" down
```

## Production environments

First time deploy

```bash
sudo chmod -R 777 ~/gaolamthuy-odoo16/addons && 
sudo chmod -R 777 ~/gaolamthuy-odoo16/etc && 
sudo mkdir -p ~/gaolamthuy-odoo16/postgresql && 
sudo chmod -R 777 ~/gaolamthuy-odoo16/postgresql && 
sudo docker-compose -f ~/gaolamthuy-odoo16/docker-compose.prod.yml up -d
```

```bash
sudo docker-compose -f ~/gaolamthuy-odoo16/docker-compose.prod.yml -p "odoo-gaolamthuy-prod" up --build --force-recreate -d
```

```bash
sudo nano ~/gaolamthuy-odoo16/.env
```

