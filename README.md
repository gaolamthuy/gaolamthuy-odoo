## Local development environments

```bash
sudo docker-compose -f ~/gaolamthuy-odoo16/docker-compose.dev.yml up --build --force-recreate -d
```

```bash
sudo chmod -R 777 ~/gaolamthuy-odoo16/addons && 
sudo chmod -R 777 ~/gaolamthuy-odoo16/etc && 
sudo mkdir -p ~/gaolamthuy-odoo16/postgresql && 
sudo chmod -R 777 ~/gaolamthuy-odoo16/postgresql && 
sudo docker-compose -f ~/gaolamthuy-odoo16/docker-compose.dev.yml up -d
```

## Staging environments

```bash
sudo docker-compose -f ~/gaolamthuy-odoo16/docker-compose.stage.yml up -d
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
sudo nano ~/gaolamthuy-odoo16/.env
```