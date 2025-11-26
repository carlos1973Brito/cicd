# Spring Boot CRUD (Java 17) + CI/CD (GitHub Actions)

Proyecto de ejemplo con:
- Java 17, Spring Boot (starter web + data-jpa)
- H2 en memoria (simple)
- Dockerfile
- GitHub Actions CI y CD (sube imagen a Docker Hub)

Rutas:
- GET  /api/persons
- GET  /api/persons/{id}
- POST /api/persons
- PUT  /api/persons/{id}
- DELETE /api/persons/{id}

Para ejecutar local:
```bash
mvn clean package
java -jar target/crud-0.0.1-SNAPSHOT.jar
```

CI/CD:
- `ci.yml` compila y ejecuta tests
- `cd.yml` construye imagen Docker y la publica en Docker Hub usando secrets DOCKER_USER y DOCKER_PASS
