Microsoft SQL Server:
docker run -d --name sql-container --network my_docker_network --restart always -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=Aptb#123" -p 1433:1433 -v sqlvolume:/var/opt/mssql -d mcr.microsoft.com/mssql/server:2019-latest
MONGOdB:<br>
docker run -it -d --name mongo-container -p 27017:27017 --network my_docker_network --restart always -v mongodb_data_container:/data/db mongo:latest<br>
NETWORK:<br>
docker network create --attachable -d bridge cqrskafkanetwork<br>
<br>
docker-compose -p cqrskafka up -d<br>
<br>
Studio 3T:<br>
https://studio3t.com/
<br>
Redis:<br>
docker run -d --cap-add sys_resource --name rp -p 8443:8443 -p 9443:9443 -p 12000:12000 redislabs/redis
<br>
Redis Desktop:<br>
https://docs.resp.app/en/latest/install/
<br>
RabbitMq:<br>
docker run -d --hostname my-rabbit --name some-rabbit -p 15672:15672 rabbitmq:3-management
<br>
Rabbit manager:<br>
http://localhost:15672/
<br>
login and password: guest