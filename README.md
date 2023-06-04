Microsoft SQL Server:
docker run -d --name sql-container --network my_docker_network --restart always -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=Aptb#123" -p 1433:1433 -v sqlvolume:/var/opt/mssql -d mcr.microsoft.com/mssql/server:2019-latest
MONGOdB:<br>
docker run -it -d --name mongo-container -p 27017:27017 --network my_docker_network --restart always -v mongodb_data_container:/data/db mongo:latest<br>
NETWORK:<br>
docker network create --attachable -d bridge cqrskafkanetwork<br>

docker-compose -p cqrskafka up -d<br>

Studio 3T:<br>
https://studio3t.com/