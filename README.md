# 🟠 Reddit Clone — Spring Boot

> A Reddit-inspired community platform built with Spring Boot 3, Spring Security, and MySQL. Features user authentication, post submission, and community browsing with a server-rendered UI — demonstrating full-stack Java MVC development with production-grade security patterns.

![Java](https://img.shields.io/badge/Java-17-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.1.3-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![Thymeleaf](https://img.shields.io/badge/Thymeleaf-3.1-005F0F?style=flat-square&logo=thymeleaf&logoColor=white)

---

## Features

- **User Auth** — Register, login, logout with Spring Security 6
- **Post Management** — Submit, view, and browse posts by community
- **Secure Routing** — Role-based access control, CSRF protection
- **Server-Side UI** — Thymeleaf templates with Spring Security dialect
- **Persistent Data** — Spring Data JPA with MySQL backend
- **Input Validation** — Request validation with Bean Validation

---

## Tech Stack

| Layer | Technology |
|---|---|
| Language | Java 17 |
| Framework | Spring Boot 3.1.3 |
| Security | Spring Security 6 |
| ORM | Spring Data JPA / Hibernate |
| Database | MySQL 8.0.31 |
| Templating | Thymeleaf 3.1 + Security Extras |
| Build | Maven |

---

## Getting Started

### Prerequisites

- Java 17+
- MySQL 8.0+
- Maven 3.6+

### Setup

```bash
git clone https://github.com/Murthyk6/Reddit_Clone.git
cd Reddit_Clone
```

Configure `src/main/resources/application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/reddit_clone
spring.datasource.username=root
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
```

Run:

```bash
./mvnw spring-boot:run
```

App starts at `http://localhost:8080`

---

## Project Structure

```
src/main/java/com/javateam/
├── controller/     # Request handlers (posts, auth, community)
├── model/          # JPA entities (User, Post, Community)
├── repository/     # Spring Data JPA interfaces
├── service/        # Business logic layer
└── security/       # Security config and UserDetailsService
src/main/resources/
├── templates/      # Thymeleaf views
└── application.properties
```

---

## Key Concepts Demonstrated

- Spring Security 6 with custom `UserDetailsService`
- Entity relationships: `@ManyToOne`, `@OneToMany` with lazy loading
- Thymeleaf Security dialect (`sec:authorize`, `sec:authentication`)
- MVC separation with controller → service → repository layers
- Form validation and BindingResult error handling

---

> Built to strengthen full-stack Java skills covering authentication, database design, and server-side rendering — patterns applied in production backend work at MountBlue and Ubona Technologies.
