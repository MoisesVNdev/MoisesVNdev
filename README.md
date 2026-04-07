# Olá, sou Moisés 👋

Desenvolvedor Backend com foco em construir sistemas **bem estruturados, testados e prontos para produção**. Aplico princípios como SOLID, arquitetura em camadas e boas práticas de segurança desde o início não como checklist, mas como forma de pensar o código.

Tenho experiência prática construindo APIs REST, sistemas distribuídos com cache e filas, PWAs offline-first e pipelines de CI/CD  tudo documentado e containerizado.

---

## 🛠️ Stack

**Linguagens**

[![Java](https://img.shields.io/badge/Java-%23ED8B00.svg?logo=openjdk&logoColor=white)](https://www.java.com)
[![TypeScript](https://img.shields.io/badge/TypeScript-%232F74C0.svg?logo=typescript&logoColor=white)](https://www.typescriptlang.org)
[![Python](https://img.shields.io/badge/Python-%233B8EB5.svg?logo=python&logoColor=white)](https://www.python.org)

**Frameworks & Libs**

[![Spring Boot](https://img.shields.io/badge/Spring_Boot-%236DB33F.svg?logo=spring&logoColor=white)](https://spring.io/projects/spring-boot)
[![Node.js](https://img.shields.io/badge/Node.js-%23339933.svg?logo=node.js&logoColor=white)](https://nodejs.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-%23009688.svg?logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![Vue 3](https://img.shields.io/badge/Vue_3-%234FC08D.svg?logo=vue.js&logoColor=white)](https://vuejs.org)

**Bancos de Dados**

[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-%23336791.svg?logo=postgresql&logoColor=white)](https://www.postgresql.org)
[![Redis](https://img.shields.io/badge/Redis-%23DC382D.svg?logo=redis&logoColor=white)](https://redis.io)
[![Cassandra](https://img.shields.io/badge/Cassandra-%231287B1.svg?logo=apachecassandra&logoColor=white)](https://cassandra.apache.org)
[![SQLite](https://img.shields.io/badge/SQLite-%23003B57.svg?logo=sqlite&logoColor=white)](https://www.sqlite.org)

**Infra & Ferramentas**

[![Docker](https://img.shields.io/badge/Docker-%232496ED.svg?logo=docker&logoColor=white)](https://www.docker.com)
[![Nginx](https://img.shields.io/badge/Nginx-%23009639.svg?logo=nginx&logoColor=white)](https://nginx.org)
[![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-%232088FF.svg?logo=githubactions&logoColor=white)](https://github.com/features/actions)
[![Git](https://img.shields.io/badge/Git-%23F05032.svg?logo=git&logoColor=white)](https://git-scm.com)
[![Linux](https://img.shields.io/badge/Linux-%23FCC624.svg?logo=linux&logoColor=black)](https://www.linux.org)

---

## 🚀 Projetos em Destaque

### 🔗 [URL Shortener System](https://github.com/MoisesVNdev/url-shortener-system)
> Sistema de encurtamento de URLs de alta performance, produção-ready e totalmente containerizado.

**Projetado para suportar 10 milhões de URLs/dia** com ratio de 10:1 leitura:escrita e retenção de 10 anos.

- **Arquitetura distribuída:** 2 réplicas FastAPI balanceadas por Nginx, cache em Redis e persistência no Apache Cassandra 5.0
- **Geração de shortcodes:** base62 com contador atômico Redis + HashIds (sem colisão entre réplicas)
- **Observabilidade completa:** Prometheus + Grafana + 4 exporters dedicados (Nginx, Redis, Cassandra, cAdvisor)
- **Testes de carga:** K6 com cenários Load, Stress e Spike documentados com métricas reais
- **Multi-stage Docker build** com usuário não-root; stack sobe com um único `docker compose up`

`Python` `FastAPI` `Apache Cassandra` `Redis` `Nginx` `Prometheus` `Grafana` `K6` `Docker`

---

### 💉 [API Carteira de Vacinação Digital](https://github.com/MoisesVNdev/api-carteira-vacinacao)
> API REST para acompanhamento vacinal familiar — segura, documentada e publicada no Docker Hub.

**Resultados reais de performance (k6):** P95 de 4,06ms com 100 VUs simultâneos, 99,84% de taxa de sucesso, zero vazamentos de memória em 15 minutos contínuos.

- **Spring Boot 4 + Java 21** com arquitetura Controller → Service → Repository e DTOs em todas as camadas
- **Segurança:** Spring Security + JWT (JJWT) + BCrypt + controle de acesso por roles
- **Banco de dados:** PostgreSQL 16 com pool HikariCP otimizado e migrações versionadas via Flyway
- **DevOps:** Multi-stage Docker build, resource limits configurados, imagem publicada no Docker Hub
- **Documentação interativa** via Swagger UI (SpringDoc OpenAPI); coleção de testes `.http` incluída

`Java 21` `Spring Boot 4` `Spring Security` `JWT` `PostgreSQL` `Flyway` `Docker` `k6`

---

### 🏪 [FiadoDigital PDV](https://github.com/MoisesVNdev/PDV-FiadoDigital)
> Sistema híbrido de Ponto de Venda offline-first para o pequeno varejo de bairro — do caderninho ao digital.

**Problema real, solução completa:** digitaliza o "fiado" com gestão de risco (bloqueio automático de inadimplentes), comunicação via WhatsApp e recibos em PDF.

- **Monorepo** com 3 pacotes (`pnpm workspaces`): Vue 3 + Vite (PWA), Express + Prisma (API REST + WebSocket), pacote shared TypeScript
- **Offline-first:** fila transacional com replay automático e idempotência via `use-offline-queue.ts`
- **Segurança:** JWT com refresh token em cookie HttpOnly + PIN gerencial (bcrypt + rate limit) nas operações críticas
- **Tempo real:** WebSocket nativo com fallback para polling
- **Testes:** Vitest (100% nos composables de domínio), Playwright E2E headless (venda, cancelamento, caixa, fiado)
- **CI/CD:** GitHub Actions com esteira lint → type-check → testes unitários → build

`Node.js` `Vue 3` `TypeScript` `SQLite` `Prisma` `WebSocket` `JWT` `Vitest` `Playwright` `Docker` `GitHub Actions`

---

## 📬 Contato

[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:moisesvn.dev@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/moisesvnoliveira/)
[![Stack Overflow](https://img.shields.io/badge/Stack_Overflow-FE7A16?style=for-the-badge&logo=stackoverflow&logoColor=white)](https://stackoverflow.com/users/32229089)
