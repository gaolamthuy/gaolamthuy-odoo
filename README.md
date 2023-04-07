## Local development environments

```bash
sudo docker-compose -f ~/gaolamthuy-odoo16/docker-compose.dev.yml up --build --force-recreate -d
```

sudo chmod -R 777 ~/gaolamthuy-odoo16/addons && 
sudo chmod -R 777 ~/gaolamthuy-odoo16/etc && 
sudo mkdir -p ~/gaolamthuy-odoo16/postgresql && 
sudo chmod -R 777 ~/gaolamthuy-odoo16/postgresql && 
sudo docker-compose -f ~/gaolamthuy-odoo16/docker-compose.dev.yml up -d