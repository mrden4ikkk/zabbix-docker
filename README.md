sudo apt update

sudo apt install docker.io -y

docker --version

docker compose version

mkdir ~/zabbix-docker
cd ~/zabbix-docker

nano docker-compose.yml

docker-compose up -d

docker ps

http://IP_СЕРВЕРА:8080
Login: Admin
Password: zabbix
________________________________________
if problem

docker logs zabbix-mysql
docker logs zabbix-server
++++++++++++++++++++++++++++

add zabbix-agent(client)

wget https://repo.zabbix.com/zabbix/7.0/ubuntu/pool/main/z/zabbix-release/zabbix-release_7.0-1+ubuntu22.04_all.deb
sudo dpkg -i zabbix-release_7.0-1+ubuntu22.04_all.deb
sudo apt update

sudo apt install zabbix-agent2
sudo nano /etc/zabbix/zabbix_agent2.conf
**************
Server=IP_СЕРВЕРА
ServerActive=IP_СЕРВЕРА
Hostname=linux-client
*************
sudo systemctl restart zabbix-agent2
