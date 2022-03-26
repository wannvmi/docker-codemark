## RabbitMQ 配置

### rabbitmq_management 地址
http://192.168.16.152:15672/ admin admin

"RabbitMQ": "host=192.168.16.152;username=admin;password=admin"

### RabbitMQ Web Server
Contexts available:
WEB-STOMP: examples
http://192.168.16.152:15670/

管理台 http://192.168.16.152:15670/

192.168.16.152:15674 admin admin

## 安装 插件 rabbitmq-plugins

docker exec rabbitmq rabbitmq-plugins list
docker exec rabbitmq rabbitmq-plugins enable rabbitmq_web_stomp rabbitmq_stomp rabbitmq_web_stomp_examples

docker-compose stop
docker-compose up -d --build

