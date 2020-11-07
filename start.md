修改 {hostname}

docker-compose up --force-recreate -d

# 安装kafka (套件: zk kafka kafka-manager)
``` bash
# 复制,解压 kafka 到 /usr/local
# 启动命令
bin/zookeeper-server-start.sh -daemon config/zookeeper.properties && bin/kafka-server-start.sh -daemon config/server.properties

cd /usr/local
git clone https://github.com/duanlinfei/kafka-docker.git
# 修改zkHost
docker-compose -f docker-compose-km.yml up -d
```
