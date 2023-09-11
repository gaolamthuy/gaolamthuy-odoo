## Local development environments

docker compose -p my-odoo-16 -f docker-compose.yml -f docker-compose.dev. up -d

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
sudo git clone -b staging https://github.com/gaolamthuy/gaolamthuy-odoo16.git ~/gaolamthuy-odoo16-stage
```

```bash
sudo nano ~/gaolamthuy-odoo16-stage/.env
```

```bash
sudo mkdir -p ~/gaolamthuy-odoo16-stage/postgresql &&
sudo mkdir -p ~/gaolamthuy-odoo16-stage/etc &&
sudo mkdir -p ~/gaolamthuy-odoo16-stage/addons &&
sudo chmod -R 777 ~/gaolamthuy-odoo16-stage/postgresql &&
sudo chmod -R 777 ~/gaolamthuy-odoo16-stage/etc &&
sudo chmod -R 777 ~/gaolamthuy-odoo16-stage/addons
```

```bash
sudo docker-compose -f ~/gaolamthuy-odoo16-stage/docker-compose.stage.yml -p "odoo-gaolamthuy-stage" up --build --force-recreate -d
```

```bash
sudo docker-compose -f ~/gaolamthuy-odoo16-stage/docker-compose.stage.yml -p "odoo-gaolamthuy-stage" down
```

_Add stack to caddy network_ - test gh actions

CD

```bash
sudo git pull
```

## Production environments

First time deploy

```bash
sudo git clone https://github.com/gaolamthuy/gaolamthuy-odoo16.git ~/gaolamthuy-odoo16-prod
```

```bash
sudo nano ~/gaolamthuy-odoo16-prod/.env
```

```bash
sudo mkdir -p ~/gaolamthuy-odoo16-prod/postgresql &&
sudo mkdir -p ~/gaolamthuy-odoo16-prod/etc &&
sudo mkdir -p ~/gaolamthuy-odoo16-prod/addons &&
sudo chmod -R 777 ~/gaolamthuy-odoo16-prod/postgresql &&
sudo chmod -R 777 ~/gaolamthuy-odoo16-prod/etc &&
sudo chmod -R 777 ~/gaolamthuy-odoo16-prod/addons
```

```bash
sudo docker-compose -f ~/gaolamthuy-odoo16-prod/docker-compose.prod.yml -p "odoo-gaolamthuy-prod" up --build --force-recreate -d
```

```bash
sudo docker-compose -f ~/gaolamthuy-odoo16-stage/docker-compose.prod.yml -p "odoo-gaolamthuy-prod" down
```

_Add stack to caddy network_ - test gh actions

CD

```bash
sudo git pull
```

After creating a new database:

```
reserved
```
