# budgetapp
	mvn package
	mvn package -DskipTests
	mvn package && java -jar target/budgetapp.jar
	mvn docker:build
	docker run -d --name budgetapp --link postgres:postgres -p 82:8080 -e DB_DRIVER=org.postgresql.Driver -e DB_USERNAME=postgres -e DB_PASSWORD=pSvCgBx4e5XbKMzX -e DB_URL=jdbc:postgresql://postgres/budget -e DB_DIALECT=io.budgetapp.hibernate.dialect.CustomPostgreSQLDialect ekotime/budgetapp
	
