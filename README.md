<h1 align="center">Natalia Cristina de Souza</h1>

<p align="center">
  <strong>Desenvolvedora de Software</strong> · Análise e Desenvolvimento de Sistemas — FIAP<br>
  Java · Spring Boot · Azure · Docker · React · SQL
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/natalia-cristina-de-souza-333b92169">LinkedIn</a>
</p>

---

## Sobre

Desenvolvedora em formação em Análise e Desenvolvimento de Sistemas pela FIAP, com
foco em **construir aplicações do banco de dados até a nuvem** — e não apenas escrever
o código do meio.

Nos últimos ciclos atuei como **representante técnica da equipe** em cinco entregas
avaliadas, responsável pela infraestrutura, pelo provisionamento na Azure e pela
publicação das aplicações. Isso significou, na prática, ser a pessoa que faz o
projeto sair do `localhost` e chegar a uma URL que funciona para quem vai avaliá-lo.

O que me interessa é o ciclo completo: modelar o domínio, expor a API, conteinerizar,
publicar, instrumentar com telemetria e corrigir o que a telemetria mostrar.

---

## Competências

| Área | Tecnologias |
|---|---|
| **Backend** | Java 17/21, Spring Boot 3, Spring Data JPA, Spring Security, Thymeleaf, Flyway, APIs REST, Swagger/OpenAPI, JUnit 5, Mockito |
| **Cloud & DevOps** | Azure App Service, Azure SQL, Azure Database for PostgreSQL, Azure Container Registry, Azure Container Instances, Application Insights, Azure CLI, Azure DevOps Pipelines, Docker, Docker Compose |
| **Front-end** | React 18, TypeScript, Vite, React Router, React Hook Form, TailwindCSS, Next.js, HTML/CSS |
| **Dados** | Oracle Database, PostgreSQL, MySQL, Azure SQL, modelagem relacional, PL/SQL, DDL/DML |
| **Python & IA** | Python 3, scikit-learn, pandas, Flask, Node-RED, modelos de classificação e clusterização |
| **Processo** | Git/GitHub, Azure Boards, planejamento de release, plano de testes, Selenium IDE |

---

## Projetos selecionados

> Os repositórios são **privados**. Concedo acesso de leitura sob solicitação —
> basta pedir pelo LinkedIn ou e-mail que eu adiciono como colaborador.

### SOLIN / Clyvo Vet — monitoramento preventivo de saúde animal
**Challenge FIAP 2026 · entrega final · representante técnica**

Plataforma que acompanha a rotina de hidratação, alimentação e excreção de pets e
dispara alertas automáticos para o tutor e para a clínica quando um indicador sai
do padrão da espécie.

- **Stack:** Java 17 · Spring Boot 3 · Spring Security · Thymeleaf · Flyway · PostgreSQL
- **Infra:** Azure App Service (Linux) + Azure Database for PostgreSQL, provisionados por script Azure CLI
- **CI/CD:** pipeline YAML no Azure DevOps, com build, testes e deploy contínuo para o App Service
- **Qualidade:** 12 casos de teste de sistema rastreados no Azure Boards, 4 automatizados em Selenium IDE, testes unitários com JUnit 5 + Mockito
- **Defeito real corrigido:** alertas duplicavam quando um evento reincidia antes da resolução do anterior. A correção passou a vincular cada alerta à regra que o originou (migration Flyway `V8`), permitindo ao serviço ignorar regras com alerta ainda pendente.

### DimDim Web — aplicação bancária com telemetria em nuvem
**Checkpoint · DevOps Tools & Cloud Computing**

Sistema de correntistas e transações (depósito, saque, Pix) com interface web e API
REST, rodando inteiramente em serviços gerenciados da Azure.

- **Stack:** Java 21 · Spring Boot 3.5 · JPA · Thymeleaf · Azure SQL Database
- **Observabilidade:** Application Insights com agente Java 3.x anexado em runtime, capturando requisições, exceções, métricas e **cada comando SQL como dependência rastreada**; diagnósticos do Azure SQL enviados ao mesmo Log Analytics
- **Segurança:** nenhuma credencial em código — connection strings e segredos vivem nas App Settings do Web App

### OrbitAgro — satélite e IoT para o agronegócio
**Global Solution FIAP 2026 · representante DevOps**

API que cruza índice **NDVI** (saúde da vegetação por imagem de satélite) com leituras
de sensores IoT de solo para gerar alertas de risco agrícola a pequenos produtores.
Alinhado aos ODS 2, 9 e 13 da ONU.

- **Stack:** Java · Spring Boot · PostgreSQL 16
- **Infra:** Docker Compose orquestrando API e banco em VM Azure

### SOLIN Sprint 3 — aplicação e banco conteinerizados
**Challenge FIAP 2026 · Sprint 3**

Mesma plataforma SOLIN, desta vez com aplicação e banco **inteiramente em containers**:
imagens publicadas no Azure Container Registry e executadas em Azure Container Instances,
com todo o provisionamento via Azure CLI e prova de persistência de dados após reinício
do container.

### Hospital Clínico — SPA de gestão hospitalar
**Challenge · Front-end**

Interface para reduzir absenteísmo hospitalar por meio de uma assistente digital que
conecta paciente, acompanhante e equipe médica.

- **Stack:** React 18 · TypeScript · Vite · React Router v6 · React Hook Form · TailwindCSS
- Rotas dinâmicas, consumo de API REST e layout responsivo

### Challenge IA — modelos preditivos com integração IoT
**Challenge · Inteligência Artificial**

Pipeline de dados com modelos de **classificação/regressão e clusterização**
(scikit-learn, serializados em `joblib`), expostos por uma API Python e integrados
a um fluxo **Node-RED** para consumo por dispositivos.

---

## Formação

**Análise e Desenvolvimento de Sistemas** — FIAP
Ênfase em arquitetura de software, computação em nuvem, DevOps e banco de dados.

---

<p align="center"><sub>
  Interessado em ver o código? Peço acesso em um minuto —
  <a href="https://www.linkedin.com/in/natalia-cristina-de-souza-333b92169">me chame no LinkedIn</a>.
</sub></p>
