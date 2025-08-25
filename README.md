# 🏦 MeuBanco API

Uma API REST desenvolvida em **Java 21** com **Spring Boot 3**, utilizando **PostgreSQL** como banco de dados e **Spring Data JPA** para persistência.  
A documentação da API é fornecida via **OpenAPI (Swagger)**.  
Deploy simplificado na nuvem com **Railway** 🚀.

---

## ✨ Funcionalidades
- CRUD de entidades do banco (exemplo: clientes, contas, transações)
- Conexão com banco **PostgreSQL**
- Documentação interativa da API com **Swagger UI**
- Configuração simplificada com **Spring Boot**

---

## 🛠️ Tecnologias Utilizadas
- **Java 21 (LTS)**
- **Spring Boot 3**
- **Spring Data JPA**
- **PostgreSQL**
- **Swagger / OpenAPI**
- **Maven**
- **Railway** (Deploy)

---

## ⚙️ Configuração do Projeto

### 🔹 Pré-requisitos
- [Java 21+](https://adoptium.net/)
- [Maven](https://maven.apache.org/)
- [PostgreSQL](https://www.postgresql.org/)
- [Git](https://git-scm.com/)

### 🔹 Clonando o repositório

git clone https://github.com/seu-usuario/meubanco-api.git
cd meubanco-api
🔹 Configurando o banco
No psql:

CREATE DATABASE meubanco;
CREATE USER meubanco_user WITH PASSWORD '123456';
GRANT ALL PRIVILEGES ON DATABASE meubanco TO meubanco_user;
🔹 Configuração application.properties
Edite src/main/resources/application.properties:

spring.datasource.url=jdbc:postgresql://localhost:5432/meubanco
spring.datasource.username=meubanco_user
spring.datasource.password=123456
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
▶️ Executando o Projeto
Com o Maven:

mvn spring-boot:run
Ou gerando o .jar:

mvn clean package
java -jar target/meubanco-0.0.1-SNAPSHOT.jar
📖 Documentação da API
Após iniciar o projeto, acesse:

👉 http://localhost:8080/swagger-ui.html

---

### 🚀 Deploy no Railway
Crie um projeto no Railway.

Configure as variáveis de ambiente:

SPRING_DATASOURCE_URL

SPRING_DATASOURCE_USERNAME

SPRING_DATASOURCE_PASSWORD

Faça o deploy com:

git push railway main

---

### 👨‍💻 Contribuição
Contribuições são bem-vindas!

Faça um fork do projeto

Crie uma branch (git checkout -b minha-feature)

Commit suas mudanças (git commit -m 'Minha nova feature')

Faça um push para a branch (git push origin minha-feature)

Abra um Pull Request 🎉
