Microsoft SQL Server:
docker run -d --name sql-container --network mydockernetwork --restart always -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=Admin@123'" -p 1434:1433 -d mcr.microsoft.com/mssql/server:2019-latest
MONGOdB:
docker run -it -d --name mongo-container -p 27017:27017 --network mydockernetwork --restart always -v mongodb_data_container:/data/db mongo:latest
NETWORK:
docker network create --attachable -d bridge cqrskafkanetwork
- testar:
	rodar sql no compose comporta diferente e a sql separado na porta default e ver se vai funcionar

docker-compose -p cqrskafka up -d



Studio 3T



docker run -d --name sql-container --network my_docker_network --restart always -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=Admin@123'" -p 1433:1433 -v sqlvolume:/var/opt/mssql -d mcr.microsoft.com/mssql/server:2019-latest
docker run -it -d --name mongo-container -p 27017:27017 --network my_docker_network --restart always -v mongodb_data_container:/data/db mongo:latest