# Spring Boot JWT Authentication example with Spring Security & Spring Data JPA

For more detail, please visit:
> [Secure Spring Boot App with Spring Security & JWT Authentication](https://dev.com/spring-boot-jwt-authentication/)

> [For MongoDB](https://dev.com/spring-boot-jwt-auth-mongodb/)

# Fullstack

> [Spring Boot + Vue.js JWT Authentication](https://dev.com/spring-boot-vue-js-authentication-jwt-spring-security/)

> [Spring Boot + Angular 8 JWT Authentication](https://dev.com/angular-spring-boot-jwt-auth/)

> [Spring Boot + React JWT Authentication](https://dev.com/spring-boot-react-jwt-auth/)

## Create database with name `wellnes-center` first

## Configure Spring Datasource, JPA, App properties
Open `src/main/resources/application.properties`
- For PostgreSQL:
```
spring.datasource.url= jdbc:postgresql://localhost:5432/wellnes-center
spring.datasource.username= postgres
spring.datasource.password= admin

spring.jpa.properties.hibernate.jdbc.lob.non_contextual_creation= true
spring.jpa.properties.hibernate.dialect= org.hibernate.dialect.PostgreSQLDialect

# Hibernate ddl auto (create, create-drop, validate, update)
spring.jpa.hibernate.ddl-auto= update

# App Properties
dev.app.jwtSecret= devSecretKey
dev.app.jwtExpirationMs= 86400000
```

## Run following SQL insert statements
```
INSERT INTO roles(name) VALUES('ROLE_USER');
INSERT INTO roles(name) VALUES('ROLE_ADMIN');
```
## Run Spring Boot application
```
mvn spring-boot:run
```



## url 
--- public
```
http://localhost:8080/api/auth/signup 
http://localhost:8080/api/auth/signin
http://localhost:8080/api/v1/all
```
--- user
```
http://localhost:8080/api/v1/user
http://localhost:8080/api/doctors (get, post, put)
http://localhost:8080/api/complaints
http://localhost:8080/api/appointments
```
---admin
```
http://localhost:8080/api/v1/admin
```
