```shell
cd apps/server/
sudo docker build -t yiluxiangbei/minidrama-server .

sudo docker rmi `docker images | grep none | awk '{print $3}'`
```