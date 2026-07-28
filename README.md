<div align="center">

![Header](https://capsule-render.vercel.app/api?type=waving&color=0:0B0E0C,100:00E676&height=200&section=header&text=Paulo%20Barbosa&fontSize=64&fontColor=F4F6F2&animation=fadeIn&desc=Tech%20Leader%20%C2%B7%20FullStack%20Engineer&descSize=22&descAlignY=75)

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Space+Grotesk&weight=600&size=22&pause=1000&color=00E676&center=true&vCenter=true&width=600&lines=10%2B+anos+construindo+software;NestJS+%C2%B7+React+%C2%B7+Next.js+%C2%B7+AWS+%C2%B7+IA;Arquitetura+multi-tenant+%26+micro+frontends;Engenharia+assistida+por+IA+com+Claude;Apaixonado+por+tecnologia%2C+business+e+design)](https://github.com/1paulobarbosa)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Paulo%20Barbosa-101511?style=for-the-badge&logo=linkedin&logoColor=00E676&labelColor=0B0E0C)](https://www.linkedin.com/in/paulo-freireb/)
[![Email](https://img.shields.io/badge/Email-paulo%40buildwithsingularity.com-101511?style=for-the-badge&logo=maildotru&logoColor=00E676&labelColor=0B0E0C)](mailto:paulo@buildwithsingularity.com)
[![Location](https://img.shields.io/badge/Curitiba-PR%2C%20Brasil-101511?style=for-the-badge&logo=googlemaps&logoColor=00E676&labelColor=0B0E0C)](#)

![Profile Views](https://komarev.com/ghpvc/?username=1paulobarbosa&color=00E676&style=flat-square&label=visitas&base=8500)

</div>

---

## SOBRE

Sou Tech Leader e engenheiro fullstack. Hoje sou o **único responsável técnico de um produto SaaS multi-tenant** — frontend, backend, cloud, segurança e IA — o que me obriga (e me diverte) a pensar o sistema inteiro como uma coisa só: regra de negócio no lugar certo, schema versionado por migration, deploy previsível e custo sob controle.

Nos últimos anos venho combinando **arquitetura de software** com **engenharia assistida por IA**: coloco modelos Claude em produção e construo agentes e workflows no Claude Code com os padrões de engenharia da empresa embutidos — automação de review, scaffolding e tarefas repetitivas caíram ~60%, sobrando tempo para o que importa: system design.

```text
o que eu faço bem
├── liderar produto técnico de ponta a ponta (frontend + backend + cloud + IA)
├── arquitetura: multi-tenant, micro frontends, pipelines assíncronos
├── apps nativos iOS — Eight (Swift · SwiftUI · SwiftData)
├── developer experience: CI/CD, IaC, Docker, agentes de IA
└── performance: do bundle ao banco, com número pra provar
```

---

## ARQUITETURA

A arquitetura que opero hoje, de ponta a ponta:

```mermaid
%%{init: {"theme":"base","themeVariables":{"background":"#0B0E0C","mainBkg":"#101511","primaryColor":"#101511","primaryTextColor":"#F4F6F2","primaryBorderColor":"#333A34","secondaryColor":"#101511","tertiaryColor":"#0B0E0C","lineColor":"#00E676","textColor":"#C7CCC8","nodeTextColor":"#F4F6F2","clusterBkg":"#0B0E0C","clusterBorder":"#1D221E","edgeLabelBackground":"#101511","fontFamily":"Space Grotesk, -apple-system, Segoe UI, sans-serif"}}}%%
flowchart TB
    subgraph Clients["FRONTENDS"]
        RETAIL["Varejo B2C<br/>React · Chakra UI"]
        PLATFORM["Plataforma<br/>React · Radix · Tailwind"]
        BACKOFFICE["Backoffice<br/>Next.js"]
    end

    subgraph API["BACKEND"]
        NEST["NestJS + TypeScript<br/>regra de negócio mora aqui"]
        AUTH["Auth · JWT · RBAC<br/>isolamento multi-tenant"]
    end

    subgraph Data["DADOS"]
        PG[("PostgreSQL<br/>TypeORM · schema só muda<br/>por migration")]
        QUEUE["Filas & Jobs<br/>processamento assíncrono"]
    end

    subgraph AI["IA EM PRODUÇÃO"]
        CLAUDE["Claude em produção<br/>governança + teto de custo"]
        AGENTS["Agentes Claude Code<br/>review · scaffolding · automação"]
    end

    subgraph Infra["INFRA & DELIVERY"]
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
    NEST --> CLAUDE
    AGENTS -. acelera o time .-> NEST
    DOCKER --> AWS
    CICD --> AWS

    classDef node fill:#101511,stroke:#333A34,color:#F4F6F2
    classDef accent fill:#101511,stroke:#00E676,color:#F4F6F2
    class RETAIL,PLATFORM,BACKOFFICE,AUTH,PG,QUEUE,DOCKER,CICD,AWS node
    class NEST,CLAUDE,AGENTS accent
```

---

## STACK

### Linguagens & Frontend
![TypeScript](https://img.shields.io/badge/TypeScript-101511?style=flat-square&logo=typescript&logoColor=00E676)
![JavaScript](https://img.shields.io/badge/JavaScript-101511?style=flat-square&logo=javascript&logoColor=00E676)
![React](https://img.shields.io/badge/React-101511?style=flat-square&logo=react&logoColor=00E676)
![Next.js](https://img.shields.io/badge/Next.js-101511?style=flat-square&logo=nextdotjs&logoColor=00E676)
![Redux](https://img.shields.io/badge/Redux%20%2F%20Context-101511?style=flat-square&logo=redux&logoColor=00E676)
![Styled Components](https://img.shields.io/badge/Styled--Components-101511?style=flat-square&logo=styledcomponents&logoColor=00E676)
![Tailwind](https://img.shields.io/badge/Tailwind-101511?style=flat-square&logo=tailwindcss&logoColor=00E676)
![HTML5](https://img.shields.io/badge/HTML%2FCSS%2FFlexbox-101511?style=flat-square&logo=html5&logoColor=00E676)

### Backend & Dados
![Node.js](https://img.shields.io/badge/Node.js-101511?style=flat-square&logo=nodedotjs&logoColor=00E676)
![NestJS](https://img.shields.io/badge/NestJS-101511?style=flat-square&logo=nestjs&logoColor=00E676)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-101511?style=flat-square&logo=postgresql&logoColor=00E676)
![TypeORM](https://img.shields.io/badge/TypeORM-101511?style=flat-square&logo=typeorm&logoColor=00E676)
![GraphQL](https://img.shields.io/badge/GraphQL-101511?style=flat-square&logo=graphql&logoColor=00E676)
![REST](https://img.shields.io/badge/REST%20APIs-101511?style=flat-square&logo=fastapi&logoColor=00E676)

### Mobile & Apps Nativos
![Swift](https://img.shields.io/badge/Swift-101511?style=flat-square&logo=swift&logoColor=00E676)
![SwiftUI](https://img.shields.io/badge/SwiftUI-101511?style=flat-square&logo=swift&logoColor=00E676)
![SwiftData](https://img.shields.io/badge/SwiftData-101511?style=flat-square&logo=swift&logoColor=00E676)
![React Native](https://img.shields.io/badge/React%20Native-101511?style=flat-square&logo=react&logoColor=00E676)

**[Eight](https://eight.buildwithsingularity.com)** — app nativo iOS + Apple Watch de equilíbrio de vida 8/8/8 (Swift · SwiftUI · SwiftData · CloudKit)

### Cloud, DevOps & Observabilidade
![AWS](https://img.shields.io/badge/AWS-101511?style=flat-square&logo=amazonwebservices&logoColor=00E676)
![Docker](https://img.shields.io/badge/Docker-101511?style=flat-square&logo=docker&logoColor=00E676)
![GitHub Actions](https://img.shields.io/badge/CI%2FCD-101511?style=flat-square&logo=githubactions&logoColor=00E676)
![New Relic](https://img.shields.io/badge/New%20Relic-101511?style=flat-square&logo=newrelic&logoColor=00E676)
![Datadog](https://img.shields.io/badge/Datadog-101511?style=flat-square&logo=datadog&logoColor=00E676)
![Git](https://img.shields.io/badge/Git-101511?style=flat-square&logo=git&logoColor=00E676)

### IA & Engenharia assistida
![Claude](https://img.shields.io/badge/Claude%20Code-101511?style=flat-square&logo=anthropic&logoColor=00E676)
![N8N](https://img.shields.io/badge/n8n-101511?style=flat-square&logo=n8n&logoColor=00E676)

### Qualidade & Arquitetura
![Jest](https://img.shields.io/badge/Jest-101511?style=flat-square&logo=jest&logoColor=00E676)
![Testing Library](https://img.shields.io/badge/React%20Testing%20Library-101511?style=flat-square&logo=testinglibrary&logoColor=00E676)
![Micro Frontends](https://img.shields.io/badge/Micro%20Frontends-Module%20Federation-101511?style=flat-square&logo=webpack&logoColor=00E676&labelColor=0B0E0C)
![Design System](https://img.shields.io/badge/Design%20System-101511?style=flat-square&logo=storybook&logoColor=00E676)
![Arquitetura](https://img.shields.io/badge/Arquitetura%20de%20Software-Multi--tenant%20%C2%B7%20Async%20%C2%B7%20IaC-101511?style=flat-square&labelColor=0B0E0C)

---

## IMPACTO EM NÚMEROS

| Resultado | Contexto |
|-----------|----------|
| **Deploy: 30min → 2min** | Workflow de CI/CD com GitHub Actions, containers reproduzíveis e ambientes isolados |
| **Imagem Docker −94%** (5GB → 279MB) | Multistage builds para aplicação Next.js |
| **Debugging −70% · MTTR reduzido** | Biblioteca de logs com request tracing (Pino.js), ativada por feature flag em produção |
| **Automação repetitiva −60%** | Agentes e workflows no Claude Code com padrões de engenharia embutidos |
| **Milhões de linhas em segundos** | Pipeline assíncrono que destravou exportação de extratos em fintech |
| **Carregamento −80%** | Otimização de performance em componentes estratégicos da plataforma |
| **Conversão +25% e +35%** | Twilio Segment (jornadas personalizadas) e busca com Algolia (<100ms) em e-commerce |
| **Core Web Vitals +65%** | Migração de Vanilla JS para JAMstack (Next.js + GraphQL) |
| **Provisionamento: dias → minutos** | Cultura de IaC — 100% dos ambientes AWS automatizados |

---

## TRAJETÓRIA

```text
2025 — hoje   GoNext          Tech Leader — produto SaaS multi-tenant B2B2C
                              (NestJS · React · AWS · Claude Code)

2024 — 2025   Lerian          Software Engineer — Core Ledger, observabilidade,
                              micro frontends (Next.js · Module Federation)

2021 — 2024   Dock            Software Engineer — fintech em escala, pipelines
                              assíncronos, performance, IaC (React · Node BFF · GraphQL)

2019 — 2021   MadeiraMadeira  Front-end Engineer — e-commerce, JAMstack,
                              Design System, Algolia, Segment

2016 — 2019   JVM             Full Stack — do requisito ao app
                              (React · React Native · PHP)
```

**Análise de Sistemas** — IFRN &nbsp;·&nbsp; **Inglês** — leitura, escrita e fala

---

## GITHUB

<div align="center">

![Stats](https://github-readme-stats-sigma-five.vercel.app/api?username=1paulobarbosa&show_icons=true&count_private=true&hide_border=true&bg_color=0B0E0C&title_color=00E676&text_color=C7CCC8&icon_color=7DFFB8&ring_color=00E676)
![Top Langs](https://github-readme-stats-sigma-five.vercel.app/api/top-langs/?username=1paulobarbosa&layout=compact&hide_border=true&bg_color=0B0E0C&title_color=00E676&text_color=C7CCC8)

![Streak](https://streak-stats.demolab.com/?user=1paulobarbosa&hide_border=true&background=0B0E0C&border=1D221E&stroke=1D221E&ring=00E676&fire=7DFFB8&currStreakNum=F4F6F2&sideNums=C7CCC8&currStreakLabel=00E676&sideLabels=8A938C&dates=5C645E)

</div>

---

## CONTRIBUIÇÕES

<div align="center">

![3D Contributions](./profile-3d-contrib/profile-singularity.svg)

![Snake animation](https://raw.githubusercontent.com/1paulobarbosa/1paulobarbosa/output/github-contribution-grid-snake-dark.svg)

</div>

---

## CONTATO

<div align="center">

*"Regra de negócio no lugar certo, schema por migration, deploy previsível."*

**Bora conversar?** → [LinkedIn](https://www.linkedin.com/in/paulo-freireb/) · [paulo@buildwithsingularity.com](mailto:paulo@buildwithsingularity.com)

![Footer](https://capsule-render.vercel.app/api?type=waving&color=0:00E676,100:0B0E0C&height=120&section=footer)

</div>
