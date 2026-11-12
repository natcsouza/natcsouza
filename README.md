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
| **Backend** | Java 17/21, Spring Boot 3, Spring Data JPA, Spring Security, Thymeleaf, Flyway, APIs REST, Swagger/OpenAPI, JUnit 5, Mockito · C# / .NET 8, ASP.NET Core, Entity Framework Core · Node.js, Express |
| **Cloud & DevOps** | Azure App Service, Azure SQL, Azure Database for PostgreSQL, Azure Container Registry, Azure Container Instances, Application Insights, Azure CLI, Azure DevOps Pipelines, Docker, Docker Compose |
| **Front-end** | React 18, TypeScript, Vite, React Router, React Hook Form, TailwindCSS, Next.js, HTML/CSS |
| **Dados** | Oracle Database, PostgreSQL, MySQL, Azure SQL, modelagem relacional, PL/SQL (packages, functions, procedures), DDL/DML |
| **Python & IA** | Python 3, scikit-learn, pandas, Flask, FastAPI, Jupyter, Node-RED, OpenCV, DeepFace, Ollama (LLM local), modelos de classificação, regressão e clusterização |
| **IoT & Embarcados** | ESP32 / ESP32-C3, Arduino (C++), sensores DHT, EEPROM, MQTT, Wokwi |
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

### AURAmed — agendamento de consultas por conversa natural
**Projeto acadêmico · IA aplicada**

Assistente que agenda consultas médicas a partir de linguagem natural, com o
**modelo de linguagem rodando localmente** em container Ollama com GPU.

- **Stack:** React + TypeScript · Express (Node) · FastAPI · Ollama · Docker Compose
- **Integrações:** Google Calendar e Google Sheets
- **A decisão central:** LLM local, não API de terceiros — nenhuma mensagem de paciente sai da máquina, que é o requisito que normalmente impede clínicas de adotarem modelos hospedados.

### E-Commerce API — .NET 8 em camadas
**CP4 · Advanced Business Development with .NET**

API de produtos e pedidos em ASP.NET Core 8, estruturada em
`Domain / Application / Infrastructure / Presentation`, com use cases, mappers e
repositórios isolados por interface.

- **Stack:** C# · .NET 8 · Entity Framework Core · Oracle
- **Qualidade:** 50 testes automatizados, health checks de liveness e de banco, Swagger

### InfluencyDB — regras de negócio em PL/SQL
**Checkpoint · Mastering Relational and Non-Relational Database**

Package Oracle que move duas regras para dentro do banco: motor de rankeamento de
influenciadores e automação de pagamento de campanha.

- A *package specification* publica só as assinaturas — a fórmula do score não é visível a quem consome
- Erros de negócio expostos como exceções nomeadas (`PRAGMA EXCEPTION_INIT`), não como códigos numéricos soltos

### IRIS — detecção de emoções com saída MQTT
**Iniciação Científica**

Classifica emoções faciais em tempo real e publica o resultado em um broker MQTT,
de onde dispositivos IoT reagem.

- **Stack:** Python · OpenCV · DeepFace · MQTT (paho)
- Inferência em thread separada da captura, para o vídeo não travar durante a classificação

### Genius — ESP32-C3
**CP1 · IoT**

Jogo da memória em hardware: 4 LEDs, botões, buzzer com nota própria por cor e três
níveis de dificuldade. Os recordes ficam gravados em **EEPROM**, sobrevivendo ao
desligamento da placa.

- **Stack:** C++ · ESP32-C3 · Wokwi

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
