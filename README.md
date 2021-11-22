# Cinema-service app
Simulate a work for buying tickets app. Introduced authorization and authentication. All incoming and outgoing data are converted to json format, also implemented global expection handler.

# Functionality
This project have multiple endpoints with admin and user access.<br/>

### **You can see them here**

POST: /register - all<br/>
GET: /cinema-halls - user/admin<br/>
POST: /cinema-halls - admin<br/>
GET: /movies - user/admin<br/>
POST: /movies - admin<br/>
GET: /movie-sessions/available - user/admin<br/>
GET: /movie-sessions/{id} - user/admin<br/>
POST: /movie-sessions - admin<br/>
PUT: /movie-sessions/{id} - admin<br/>
DELETE: /movie-sessions/{id} - admin<br/>
GET: /orders - user<br/>
POST: /orders/complete - user<br/>
PUT: /shopping-carts/movie-sessions - user<br/>
GET: /shopping-carts/by-user - user<br/>
GET: /users/by-email - admin<br/>

```java
/register  {"email":"email@gmail.com", "password":"password", "repeatPassword":"password"}  POST
/cinema-halls  {"capacity":255, "description":"One-Byte hall"}  POST
/movies  {"title":"Harry Potter", "description":"Nice movie"}  POST
 
/movie-sessions/available  ?movieId={id}&date=dd.MM.yyyy  GET
/movie-sessions  {"movieId":1, "cinemaHallId":1, "showTime":"21.11.2021 20:15"}  POST
/movie-sessions/{id}  {"movieId":1, "cinemaHallId":1, "showTime":"21.11.2021 20:15"}  PUT
/shopping-carts/movie-sessions  ?movieSessionId=1  PUT
/users/by-email  ?email=yourmail  GET
 ```

# Technologies Used:
- Java 11
- Maven Checkstyle Plugin
- Spring Framework
- Hibernate
- REST
- Apache Tomcat
- MySQL RDBMS

# Running the Project:

1. Сlone this project.

2. Install [Apache Tomcat](https://tomcat.apache.org/download-90.cgi)® version 9.0.54 or latest on your computer as a web server.

3. You need is relational database like MySQL or PostgreSQL:

```java
#Database properties
db.driver= DB DRIVER
db.url=DB URL
db.user=YOUR USERNAME
db.password=YOUR PASSWORD
#Hibernate properties
hibernate.show_sql=true
hibernate.hbm2ddl.auto=create
hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
```
