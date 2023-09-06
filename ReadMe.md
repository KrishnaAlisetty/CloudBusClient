Install RabbitMQ

docker pull rabbitmq:management
docker run -d --name dev-rabbit --hostname localhost -p 15672:15672 -p 5672:5672 rabbitmq:management

docker ps
docker logs -f dev-rabbit

Login to RabbitMQ
http://localhost:15672 ( guest/guest) 

visit localhost:8080/app/message

Go to nw-configrepo and edit service.message
 Do POST http://localhost:8888/actuator/busrefresh
 
 and now visit localhost:8080/app/message to see updated message 
