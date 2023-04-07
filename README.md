## Local development environments

```bash
sudo docker-compose -f ~/gaolamthuy-odoo16/docker-compose.dev.yml -p "odoo-gaolamthuy-dev" up --build --force-recreate -d
```

```bash
sudo docker-compose -f ~/gaolamthuy-odoo16/docker-compose.dev.yml -p "odoo-gaolamthuy-dev" down
```

```bash
sudo chmod -R 777 ~/gaolamthuy-odoo16/addons && 
sudo chmod -R 777 ~/gaolamthuy-odoo16/etc && 
sudo mkdir -p ~/gaolamthuy-odoo16/postgresql && 
sudo chmod -R 777 ~/gaolamthuy-odoo16/postgresql
```

## Staging environments

```bash
sudo docker-compose -f ~/gaolamthuy-odoo16/docker-compose.stage.yml -p "odoo-gaolamthuy-stage" up --build --force-recreate -d
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