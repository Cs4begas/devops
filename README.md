1. ` docker run -it --rm -d -v mysql_data:/var/lib/mysql -v mysql_config:/etc/mysql/conf.d --network mysqlnet --name mysqlserver -e MYSQL_USER=petclinic -e MYSQL_PASSWORD=petclinic -eMYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=petclinic -p 3306:3306 mysql:8.0`

2. `docker run --name spring-boot-mysql --network mysqlnet -e MYSQL_URL=jdbc:mysql://mysqlserver/petclinic -p 6060:6060 java-petclinic`