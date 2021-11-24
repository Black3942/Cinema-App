# Cinema-service app
Simple app - simulate a work for buying tickets. Introduced authorization and authentication. All incoming and outgoing data are converted to json format, also implemented global expection handler.

# Functionality
This project have multiple endpoints with several access roles.<br/>

### **You can see them here**

GET:
- /cinema-halls - user/admin<br/>
- /movies - user/admin<br/>
- /movie-sessions/available - user/admin<br/>
- /movie-sessions/{id} - user/admin<br/>
- /orders - user<br/>
- /shopping-carts/by-user - user<br/>
- /users/by-email - admin<br/>

POST: 
- /register - all<br/>
- /cinema-halls - admin<br/>
- /movies - admin<br/>
- /movie-sessions - admin<br/>
- /orders/complete - user<br/>

PUT: 
- /movie-sessions/{id} - admin<br/>
- /shopping-carts/movie-sessions - user<br/>

DELETE:
- /movie-sessions/{id} - admin<br/>

```java
GET:
/movie-sessions/available  ?movieId={id}&date=dd.MM.yyyy
/users/by-email  ?email=yourmail

POST:
/register  {"email":"email@gmail.com", "password":"password", "repeatPassword":"password"}
/cinema-halls  {"capacity":255, "description":"One-Byte hall"}
/movies  {"title":"Harry Potter", "description":"Nice movie"}
/movie-sessions  {"movieId":1, "cinemaHallId":1, "showTime":"21.11.2021 20:15"}
 
PUT:
/movie-sessions/{id}  {"movieId":1, "cinemaHallId":1, "showTime":"21.11.2021 20:15"}
/shopping-carts/movie-sessions  ?movieSessionId=1

DELETE:
/movie-sessions/{id} ?id=1
 ```

# Technologies Used:
- Java 11
- Maven Checkstyle Plugin
- Spring Framework (Core, Web and Security)
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
