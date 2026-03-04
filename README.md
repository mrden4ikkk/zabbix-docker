docker --version
docker compose version

mkdir ~/zabbix-docker
cd ~/zabbix-docker

nano docker-compose.yml

docker compose up -d

docker ps

http://IP_СЕРВЕРА:8080
Login: Admin
Password: zabbix
________________________________________
if problem

docker logs zabbix-mysql
docker logs zabbix-server


