<div align="center">

![Header](https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=200&section=header&text=Paulo%20Barbosa&fontSize=64&fontColor=ffffff&animation=fadeIn&desc=Tech%20Leader%20%C2%B7%20FullStack%20Engineer&descSize=22&descAlignY=75)

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=61DAFB&center=true&vCenter=true&width=600&lines=9%2B+anos+construindo+produtos+de+ponta+a+ponta;NestJS+%C2%B7+React+%C2%B7+Next.js+%C2%B7+AWS+%C2%B7+IA;Arquitetura+multi-tenant+%26+micro+frontends;Engenharia+assistida+por+IA+com+Claude;Apaixonado+por+tecnologia%2C+business+e+design)](https://github.com/1paulobarbosa)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Paulo%20Barbosa-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/paulobarbosa)
[![Email](https://img.shields.io/badge/Email-paulo%40buildwithsingularity.com-EA4335?style=for-the-badge&logo=maildotru&logoColor=white)](mailto:paulo@buildwithsingularity.com)
[![Location](https://img.shields.io/badge/Curitiba-PR%2C%20Brasil-2E7D32?style=for-the-badge&logo=googlemaps&logoColor=white)](#)

![Profile Views](https://komarev.com/ghpvc/?username=1paulobarbosa&color=61DAFB&style=flat-square&label=visitas)

</div>

---

## 🧭 Sobre mim

<img align="right" width="340" src="https://raw.githubusercontent.com/abhisheknaiidu/awesome-github-profile-readme/master/gifs/coder.gif" alt="Coding GIF" />

Sou Tech Leader e engenheiro fullstack. Hoje sou o **único responsável técnico de um produto SaaS multi-tenant** — frontend, backend, cloud, segurança e IA — o que me obriga (e me diverte) a pensar o sistema inteiro como uma coisa só: regra de negócio no lugar certo, schema versionado por migration, deploy previsível e custo sob controle.

Nos últimos anos venho combinando **arquitetura de software** com **engenharia assistida por IA**: coloco modelos Claude em produção via AWS Bedrock e construo agentes e workflows no Claude Code com os padrões de engenharia da empresa embutidos — automação de review, scaffolding e tarefas repetitivas caíram ~60%, sobrando tempo para o que importa: system design.

```text
o que eu faço bem
├── liderar produto técnico de ponta a ponta (frontend + backend + cloud + IA)
├── arquitetura: multi-tenant, micro frontends, pipelines assíncronos
├── developer experience: CI/CD, IaC, Docker, agentes de IA
└── performance: do bundle ao banco, com número pra provar
```

<br clear="right" />

---

## 🏗️ Como eu penso um sistema

A arquitetura que opero hoje, de ponta a ponta:

```mermaid
flowchart TB
    subgraph Clients["🖥️ Frontends"]
        RETAIL["Varejo B2C<br/>React · Chakra UI"]
        PLATFORM["Plataforma<br/>React · Radix · Tailwind"]
        BACKOFFICE["Backoffice<br/>Next.js"]
    end

    subgraph API["⚙️ Backend"]
        NEST["NestJS + TypeScript<br/>regra de negócio mora aqui"]
        AUTH["Auth · JWT · RBAC<br/>isolamento multi-tenant"]
    end

    subgraph Data["🗄️ Dados"]
        PG[("PostgreSQL<br/>TypeORM · schema só muda<br/>por migration")]
        QUEUE["Filas & Jobs<br/>processamento assíncrono"]
    end

    subgraph AI["🤖 IA em produção"]
        BEDROCK["AWS Bedrock · Claude<br/>governança + teto de custo"]
        AGENTS["Agentes Claude Code<br/>review · scaffolding · automação"]
    end

    subgraph Infra["☁️ Infra & Delivery"]
        DOCKER["Docker<br/>containers reproduzíveis"]
        CICD["GitHub Actions<br/>deploy 30min → 2min"]
        AWS["AWS<br/>ambientes isolados · IaC"]
    end

    RETAIL --> NEST
    PLATFORM --> NEST
    BACKOFFICE --> NEST
    NEST --> AUTH
    NEST --> PG
    NEST --> QUEUE
    NEST --> BEDROCK
    AGENTS -. acelera o time .-> NEST
    DOCKER --> AWS
    CICD --> AWS
```

---

## 🧰 Stack & Expertise

<div align="center">

[![Skills](https://skillicons.dev/icons?i=ts,js,react,nextjs,redux,tailwind,styledcomponents,html,css&perline=9)](https://skillicons.dev)
[![Skills](https://skillicons.dev/icons?i=nodejs,nestjs,postgres,graphql,aws,docker,githubactions,jest,git&perline=9)](https://skillicons.dev)

</div>

### Linguagens & Frontend
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Redux](https://img.shields.io/badge/Redux%20%2F%20Context-764ABC?style=flat-square&logo=redux&logoColor=white)
![Styled Components](https://img.shields.io/badge/Styled--Components-DB7093?style=flat-square&logo=styledcomponents&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML%2FCSS%2FFlexbox-E34F26?style=flat-square&logo=html5&logoColor=white)

### Backend & Dados
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![TypeORM](https://img.shields.io/badge/TypeORM-FE0803?style=flat-square&logo=typeorm&logoColor=white)
![GraphQL](https://img.shields.io/badge/GraphQL-E10098?style=flat-square&logo=graphql&logoColor=white)
![REST](https://img.shields.io/badge/REST%20APIs-005571?style=flat-square&logo=fastapi&logoColor=white)

### Cloud, DevOps & Observabilidade
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/CI%2FCD-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![New Relic](https://img.shields.io/badge/New%20Relic-1CE783?style=flat-square&logo=newrelic&logoColor=black)
![Datadog](https://img.shields.io/badge/Datadog-632CA6?style=flat-square&logo=datadog&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

### IA & Engenharia assistida
![Claude](https://img.shields.io/badge/Claude%20Code-D97757?style=flat-square&logo=anthropic&logoColor=white)
![Bedrock](https://img.shields.io/badge/AWS%20Bedrock-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![N8N](https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white)

### Qualidade & Arquitetura
![Jest](https://img.shields.io/badge/Jest-C21325?style=flat-square&logo=jest&logoColor=white)
![Testing Library](https://img.shields.io/badge/React%20Testing%20Library-E33332?style=flat-square&logo=testinglibrary&logoColor=white)
![Micro Frontends](https://img.shields.io/badge/Micro%20Frontends-Module%20Federation-8B5CF6?style=flat-square&logo=webpack&logoColor=white)
![Design System](https://img.shields.io/badge/Design%20System-FF4785?style=flat-square&logo=storybook&logoColor=white)
![Arquitetura](https://img.shields.io/badge/Arquitetura%20de%20Software-Multi--tenant%20%C2%B7%20Async%20%C2%B7%20IaC-0F766E?style=flat-square)

---

## 📈 Impacto em números

| 🎯 | Resultado | Contexto |
|----|-----------|----------|
| 🚀 | **Deploy: 30min → 2min** | Workflow de CI/CD com GitHub Actions, containers reproduzíveis e ambientes isolados |
| 📦 | **Imagem Docker −94%** (5GB → 279MB) | Multistage builds para aplicação Next.js |
| 🔎 | **Debugging −70% · MTTR reduzido** | Biblioteca de logs com request tracing (Pino.js), ativada por feature flag em produção |
| 🤖 | **Automação repetitiva −60%** | Agentes e workflows no Claude Code com padrões de engenharia embutidos |
| ⚡ | **Milhões de linhas em segundos** | Pipeline assíncrono que destravou exportação de extratos em fintech |
| 🖥️ | **Carregamento −80%** | Otimização de performance em componentes estratégicos da plataforma |
| 🛒 | **Conversão +25% e +35%** | Twilio Segment (jornadas personalizadas) e busca com Algolia (<100ms) em e-commerce |
| 🌐 | **Core Web Vitals +65%** | Migração de Vanilla JS para JAMstack (Next.js + GraphQL) |
| ☁️ | **Provisionamento: dias → minutos** | Cultura de IaC — 100% dos ambientes AWS automatizados |

---

## 💼 Trajetória

```text
2025 — hoje   GoNext          Tech Leader — produto SaaS multi-tenant B2B2C
                              (NestJS · React · AWS · Bedrock · Claude Code)

2024 — hoje   Lerian          Software Engineer — Core Ledger, observabilidade,
                              micro frontends (Next.js · Module Federation)

2021 — 2024   Dock            Software Engineer — fintech em escala, pipelines
                              assíncronos, performance, IaC (React · Node BFF · GraphQL)

2019 — 2021   MadeiraMadeira  Front-end Engineer — e-commerce, JAMstack,
                              Design System, Algolia, Segment

2016 — 2019   JVM             Full Stack — do requisito ao app
                              (React · React Native · PHP)
```

🎓 **Análise de Sistemas** — IFRN &nbsp;·&nbsp; 🌎 **Inglês** — leitura, escrita e fala

---

## 📊 GitHub

<div align="center">

![Stats](https://github-readme-stats.vercel.app/api?username=1paulobarbosa&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=1paulobarbosa&layout=compact&theme=tokyonight&hide_border=true)

![Streak](https://github-readme-streak-stats.herokuapp.com/?user=1paulobarbosa&theme=tokyonight&hide_border=true)

</div>

---

## 🏙️ Contribuições em 3D

<div align="center">

![3D Contributions](./profile-3d-contrib/profile-night-rainbow.svg#gh-dark-mode-only)
![3D Contributions](./profile-3d-contrib/profile-green-animate.svg#gh-light-mode-only)

</div>

---

## 🐍 Contribution Snake

<div align="center">

![Snake animation](https://raw.githubusercontent.com/1paulobarbosa/1paulobarbosa/output/github-contribution-grid-snake-dark.svg#gh-dark-mode-only)
![Snake animation](https://raw.githubusercontent.com/1paulobarbosa/1paulobarbosa/output/github-contribution-grid-snake.svg#gh-light-mode-only)

</div>

---

<div align="center">

*"Regra de negócio no lugar certo, schema por migration, deploy previsível."*

**Bora conversar?** → [LinkedIn](https://www.linkedin.com/in/paulobarbosa) · [paulo@buildwithsingularity.com](mailto:paulo@buildwithsingularity.com)

![Footer](https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=120&section=footer)

</div>
