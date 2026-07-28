<div align="center">

![Header](https://capsule-render.vercel.app/api?type=waving&color=0:0B0E0C,100:00E676&height=200&section=header&text=Paulo%20Barbosa&fontSize=64&fontColor=F4F6F2&animation=fadeIn&desc=Consultor%20%C2%B7%20FullStack%20Engineer&descSize=22&descAlignY=75)

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Space+Grotesk&weight=600&size=22&pause=1000&color=00E676&center=true&vCenter=true&width=600&lines=10%2B+anos+construindo+software;NestJS+%C2%B7+React+%C2%B7+Next.js+%C2%B7+AWS+%C2%B7+IA;Arquitetura+multi-tenant+%26+micro+frontends;Engenharia+assistida+por+IA+com+Claude;Apaixonado+por+tecnologia%2C+business+e+design)](https://github.com/1paulobarbosa)

[![Site](https://img.shields.io/badge/Site-paulobarbosa.dev-101511?style=for-the-badge&logo=googlechrome&logoColor=00E676&labelColor=0B0E0C)](https://paulobarbosa.dev)
[![Singularity](https://img.shields.io/badge/Studio-buildwithsingularity.com-101511?style=for-the-badge&logo=rocket&logoColor=00E676&labelColor=0B0E0C)](https://buildwithsingularity.com)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Paulo%20Barbosa-101511?style=for-the-badge&logoColor=00E676&labelColor=0B0E0C)](https://www.linkedin.com/in/paulo-freireb/)
[![Email](https://img.shields.io/badge/Email-paulo%40buildwithsingularity.com-101511?style=for-the-badge&logo=maildotru&logoColor=00E676&labelColor=0B0E0C)](mailto:paulo@buildwithsingularity.com)
[![Location](https://img.shields.io/badge/Curitiba-PR%2C%20Brasil-101511?style=for-the-badge&logo=googlemaps&logoColor=00E676&labelColor=0B0E0C)](#)

![Profile Views](https://komarev.com/ghpvc/?username=1paulobarbosa&color=00E676&style=flat-square&label=visitas&base=8500)

</div>

---

## SOBRE

Sou consultor e engenheiro fullstack, e fundador do **[Singularity](https://buildwithsingularity.com)** — um product studio focado em transformar produto em faturamento.

Seis casas, quatro domínios bem diferentes. Comecei em e-commerce — varejo online de casa e construção, catálogo enorme e pico de tráfego concentrado em data comemorativa. De lá fui pra infraestrutura de pagamentos: emissão de cartão e banking as a service, o tipo de sistema que outros produtos usam de alicerce. Duas escolas opostas — uma te ensina o que volume faz com código escrito com pressa, a outra te ensina que errar custa o dinheiro de alguém.

Depois vieram viagens, numa plataforma de venda de passagem em escala, e logística de last-mile, ligando loja física a marketplace pra entrega rápida. Operação de verdade: quando o sistema cai, alguém sente na mesma hora. Em seguida, core banking open source — a primeira vez que o código que eu escrevia era lido por gente de fora da empresa, e isso muda o padrão de cuidado.

O Singularity é a soma de tudo isso: em algum ponto do caminho ficou claro pra mim que **o gargalo quase nunca é técnico**.

Em paralelo, venho combinando **arquitetura de software** com **engenharia assistida por IA**: coloco modelos Claude em produção e construo agentes e workflows no Claude Code com os padrões de engenharia do time embutidos — automação de review, scaffolding e tarefas repetitivas caíram ~60%, sobrando tempo para o que importa: system design.

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

Uma arquitetura que desenhei e opero de ponta a ponta:

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
![AWS](https://img.shields.io/badge/AWS-101511?style=flat-square&logoColor=00E676)
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
por onde passei
├── e-commerce           varejo online de casa e construção — catálogo enorme,
│                        pico de tráfego concentrado em data comemorativa
│
├── pagamentos           emissão de cartão e banking as a service — o tipo de
│                        sistema que outros produtos usam de alicerce
│
├── viagens              venda de passagem em escala
│
├── logística last-mile  loja física ligada a marketplace pra entrega rápida —
│                        quando o sistema cai, alguém sente na mesma hora
│
├── core banking OSS     código lido por gente de fora da empresa,
│                        e isso muda o padrão de cuidado
│
└── hoje                 consultoria + Singularity, product studio
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

[paulobarbosa.dev](https://paulobarbosa.dev) &nbsp;·&nbsp; [buildwithsingularity.com](https://buildwithsingularity.com)

**Bora conversar?** → [LinkedIn](https://www.linkedin.com/in/paulo-freireb/) · [paulo@buildwithsingularity.com](mailto:paulo@buildwithsingularity.com)

![Footer](https://capsule-render.vercel.app/api?type=waving&color=0:00E676,100:0B0E0C&height=120&section=footer)

</div>
