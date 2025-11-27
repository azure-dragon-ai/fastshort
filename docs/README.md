```shell
cd apps/server
sudo docker build -t yiluxiangbei/minidrama-server .

cd apps/admin
sudo docker build -t yiluxiangbei/minidrama-admin .

sudo docker compose start mongodb
sudo docker compose up -d

sudo docker rmi `docker images | grep none | awk '{print $3}'`
```