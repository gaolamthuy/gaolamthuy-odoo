## Local development environments

```bash
sudo docker-compose -f ~/gaolamthuy-odoo16/docker-compose.dev.yml -p "odoo-gaolamthuy-dev" up --build --force-recreate -d
```

```bash
sudo docker-compose -f ~/gaolamthuy-odoo16/docker-compose.dev.yml -p "odoo-gaolamthuy-dev" down
```

```bash
sudo mkdir -p ~/gaolamthuy-odoo16/postgresql && 
sudo chmod -R 777 ~/gaolamthuy-odoo16/postgresql &&
sudo chmod -R 777 ~/gaolamthuy-odoo16/etc && 
sudo chmod -R 777 ~/gaolamthuy-odoo16/addons
```

## Staging environments

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

```bash
sudo rm -rf ~/gaolamthuy-odoo16/etc/dev/addons
sudo rm -rf ~/gaolamthuy-odoo16/etc/dev/filestore
sudo rm -rf ~/gaolamthuy-odoo16/etc/dev/sessions
sudo rm -rf ~/gaolamthuy-odoo16/etc/stage/addons
sudo rm -rf ~/gaolamthuy-odoo16/etc/stage/filestore
sudo rm -rf ~/gaolamthuy-odoo16/etc/stage/sessions
sudo rm -rf ~/gaolamthuy-odoo16/etc/prod/addons
sudo rm -rf ~/gaolamthuy-odoo16/etc/prod/filestore
sudo rm -rf ~/gaolamthuy-odoo16/etc/prod/sessions
```