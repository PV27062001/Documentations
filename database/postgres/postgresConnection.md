# Spring Boot PostgreSQL Example

This is a simple Spring Boot application that demonstrates how to create a table in a PostgreSQL database using a `schema.sql` file.

## Prerequisites

- Java 17 or later
- Gradle
- PostgreSQL

## Getting Started

### 1. Clone the Repository

```sh
git clone https://github.com/your-username/spring-boot-postgresql-example.git
cd spring-boot-postgresql-example

spring.sql.init.schema-locations=classpath:schema.sql
spring.datasource.url=jdbc:postgresql://localhost:5432/yourdatabase
spring.datasource.username=yourusername
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=none
spring.sql.init.mode = always
```

## build.gradle file

```sh
dependencies {
    implementation 'org.springframework.boot:spring-boot-starter-data-jpa'
    implementation 'org.springframework.boot:spring-boot-starter-web'
    runtimeOnly 'org.postgresql:postgresql'
    testImplementation 'org.springframework.boot:spring-boot-starter-test'
}
```
## APPLICATION STRUCTURE
```sh
spring-boot-postgresql-example
├── build.gradle
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com
│   │   │       └── example
│   │   │           └── demo
│   │   │               ├── DemoApplication.java
│   │   ├── resources
│   │       ├── application.properties
│   │       └── schema.sql
└── README.md
```