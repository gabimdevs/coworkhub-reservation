[![Typing SVG](https://readme-typing-svg.herokuapp.com/?color=7209b7&size=35&center=true&vCenter=true&width=1000&lines=+Bem+vindo+ao+CoWork+Hub!+)](https://git.io/typing-svg)


Sistema de reservas para espaços de coworking, desenvolvido em **Java Spring Boot**.

## 🧑‍💻 Integrantes
+ Gabriela Gomes Cezar RM556941

## 🚀 Tecnologias

* Java 17+
* Spring Boot
* Spring Security (OAuth2 - GitHub)
* Gradle (Kotlin DSL)
* Docker & Docker Compose
* H2 Database (desenvolvimento)

---

## 📂 Estrutura do Projeto

```
coworkhub-reservation-main/
├── src/main/java/...    # Código fonte (Controllers, Services, Repositories)
├── src/main/resources/  # Configurações (application.properties, templates)
├── build.gradle.kts     # Configuração do Gradle
├── docker-compose.yml   # Orquestração com Docker
├── Dockerfile           # Build da aplicação em container
├── .env.example         # Variáveis de ambiente de exemplo
└── README.md            # Este arquivo
```

---

## ⚙️ Pré-requisitos

Antes de rodar o projeto, instale:

* [Java 17+](https://adoptium.net/)
* [Gradle](https://gradle.org/) (ou use o wrapper `./gradlew`)
* [Docker](https://www.docker.com/) e [Docker Compose](https://docs.docker.com/compose/)

---

## ▶️ Rodando o projeto localmente

### 1. Clone o repositório

```bash
git clone https://github.com/gabimmdev/coworkhub-reservation.git
cd coworkhub-reservation-main
```

### 2. Configure variáveis de ambiente

Copie o arquivo `.env.example` para `.env` e ajuste conforme necessário:

```bash
cp .env.example .env
```

Exemplo de variáveis:

```ini
GITHUB_CLIENT_ID=seu-client-id
GITHUB_CLIENT_SECRET=seu-client-secret
SPRING_DATASOURCE_URL=jdbc:h2:mem:testdb
SPRING_DATASOURCE_USERNAME=sa
SPRING_DATASOURCE_PASSWORD=
```

### 3. Rodar com Gradle Wrapper

No Linux/Mac:

```bash
./gradlew bootRun
```

No Windows:

```bash
gradlew.bat bootRun
```

A aplicação estará disponível em: [http://localhost:8080](http://localhost:8080)

---

## 🐳 Rodando com Docker

### Build da imagem

```bash
docker build -t coworkhub-reservation .
```

### Subir com docker-compose

```bash
docker-compose up --build
```

A aplicação estará rodando em: [http://localhost:8080](http://localhost:8080)

---

## 🧪 Rodando os testes

```bash
./gradlew test
```

---

## 🔑 Autenticação via GitHub OAuth

Este projeto suporta login via GitHub OAuth. Veja o guia em [GITHUB_OAUTH_SETUP.md](GITHUB_OAUTH_SETUP.md) para configurar seu `client_id` e `client_secret`.

---

## 📖 Endpoints principais

* `/` - Página inicial
* `/workspaces` - Listagem de espaços de coworking
* `/reservations` - Reservas do usuário
* `/login` - Login via OAuth GitHub

---

## 👨‍💻 Contribuição

1. Fork o projeto
2. Crie uma branch (`git checkout -b feature/nova-feature`)
3. Commit suas alterações (`git commit -m 'Adiciona nova feature'`)
4. Push para a branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

---
## Para executar

```bash
docker compose up --build
```
