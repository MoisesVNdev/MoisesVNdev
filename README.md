# Olá, sou Moisés 👋

**Desenvolvedor Backend Java** em busca da minha primeira oportunidade como **Júnior**.
📍 Caruaru, PE · Aberto a remoto ou híbrido

Construo APIs REST com **Java 21 e Spring Boot**: autenticação com Spring Security e JWT, persistência com JPA, PostgreSQL e Flyway, tudo containerizado com Docker. Gosto de **medir** o que construo. Por isso meus projetos têm testes de carga com k6, métricas com Prometheus e Grafana e decisões técnicas documentadas.

- 🎓 Tecnólogo em Análise e Desenvolvimento de Sistemas, UniNassau (2023–2025) <!-- VERIFICAR: confirme "Tecnólogo" no diploma -->
- 🌎 Inglês básico, com leitura de documentação técnica
- 📚 Estudando agora: testes de integração com Testcontainers e mensageria com RabbitMQ/Kafka

---

## 🛠️ Stack

**Principal**

[![Java](https://img.shields.io/badge/Java_21-%23ED8B00.svg?logo=openjdk&logoColor=white)](https://www.java.com)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-%236DB33F.svg?logo=spring&logoColor=white)](https://spring.io/projects/spring-boot)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-%23336791.svg?logo=postgresql&logoColor=white)](https://www.postgresql.org)
[![Docker](https://img.shields.io/badge/Docker-%232496ED.svg?logo=docker&logoColor=white)](https://www.docker.com)
[![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-%232088FF.svg?logo=githubactions&logoColor=white)](https://github.com/features/actions)
[![Git](https://img.shields.io/badge/Git-%23F05032.svg?logo=git&logoColor=white)](https://git-scm.com)

**Também já usei em projetos**

`TypeScript / Node.js (Express, Prisma)` · `Python (FastAPI)` · `Redis` · `Cassandra` · `SQLite` · `Nginx` · `Prometheus` · `Grafana` · `k6` · `Vue 3` · `Linux`

---

## 🚀 Projetos em destaque

### 💉 [API Carteira de Vacinação Digital](https://github.com/MoisesVNdev/api-carteira-vacinacao) · Java / Spring Boot
> API REST para pais e responsáveis acompanharem o calendário vacinal da família.

- **Java 21 + Spring Boot**, em camadas (Controller → Service → Repository), com DTOs e tratamento global de exceções
- **Segurança:** Spring Security + JWT, senhas com BCrypt, segredos só em variáveis de ambiente e controle de acesso por posse dos dados: cada usuário só acessa as pessoas vinculadas a ele (proteção contra IDOR)
- **Dados:** PostgreSQL 16 com 6 migrações Flyway, incluindo a carga do calendário do PNI
- **Performance medida (k6, ambiente local):** P95 de 4 ms com 100 usuários virtuais e 0,12% de erro HTTP
- **Docker:** build multi-stage e multi-arquitetura (amd64/arm64), container sem root, [imagem publicada no Docker Hub](https://hub.docker.com/r/moisesvn/carteira-vacinacao-api)

`Java 21` `Spring Boot` `Spring Security` `JWT` `JPA` `PostgreSQL` `Flyway` `Docker` `k6`

---

### 🏪 [FiadoDigital PDV](https://github.com/MoisesVNdev/PDV-FiadoDigital) · Node.js / TypeScript
> Ponto de venda offline-first que substitui o "caderninho do fiado" do pequeno comércio.

<!-- VERIFICAR: se algum comércio usa o sistema de verdade, troque a linha abaixo por "Em uso em [nome/tipo do comércio] desde [mês/ano]". Isso é o seu maior diferencial. -->
- **API REST + WebSocket** em Express e Prisma, com regras de negócio de crédito: limite por cliente e bloqueio automático de inadimplentes
- **Offline-first:** fila de vendas com reenvio automático e idempotência por UUID, para nenhuma venda se perder nem duplicar sem rede
- **Consistência:** transações no Prisma em venda no fiado, pagamento de dívida, cancelamento e estorno
- **Segurança:** controle de acesso por perfil (admin, gerente, operador, estoquista), access token em memória + refresh token em cookie HttpOnly e PIN gerencial (bcrypt + rate limit) nas operações financeiras
- **Qualidade:** testes com Vitest e E2E com Playwright <!-- depois do commit do .github/workflows/ci.yml, acrescente: "e CI no GitHub Actions" -->

`Node.js` `TypeScript` `Express` `Prisma` `SQLite` `WebSocket` `Vitest` `Playwright`

---

### 🔗 [URL Shortener System](https://github.com/MoisesVNdev/url-shortener-system) · Python / FastAPI
> Encurtador de URLs dimensionado para alto volume de leitura, com cache, balanceamento e observabilidade.

- **2 réplicas da API** atrás do Nginx, **cache Redis** para as leituras e **Cassandra** para a persistência
- **Códigos curtos sem colisão** entre réplicas, gerados por contador atômico no Redis + HashIds (base62)
- **Observabilidade:** Prometheus + Grafana com 4 exporters (Nginx, Redis, Cassandra, cAdvisor)
- **Performance medida (k6, ambiente local):** 1.352 req/s sustentadas no stress test (1,2 milhão de requisições, 1 erro), P95 de 117 ms
- **Docker:** [imagem da API no Docker Hub](https://hub.docker.com/r/moisesvn/url-shortener-api); a stack inteira sobe com um `docker compose up`

`Python` `FastAPI` `Redis` `Cassandra` `Nginx` `Prometheus` `Grafana` `k6` `Docker`

---

## 📬 Contato

[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:moisesvn.dev@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/moisesvnoliveira/)
[![Docker Hub](https://img.shields.io/badge/Docker_Hub-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://hub.docker.com/u/moisesvn)
[![Stack Overflow](https://img.shields.io/badge/Stack_Overflow-FE7A16?style=for-the-badge&logo=stackoverflow&logoColor=white)](https://stackoverflow.com/users/32229089)
