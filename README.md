# Firmansyah Otoluwa

## Full-Stack TypeScript Engineer

I build AI-agent workflows, serverless SaaS, and privacy-first desktop products.

**React** · **Next.js** · **TypeScript** · **Node.js** · **AWS Amplify Gen 2** · **Electron** · **MCP**

Open to remote full-stack, product engineering, and AI-agent platform opportunities.

## Featured Work

- [**Flowtive**](https://github.com/programmerlapar/flowtive-app) - Offline-first project management for Kanban, sprints, analytics, LAN sync, and AI-agent collaboration. Available on the web, desktop, Chrome, VS Code, and MCP clients.
- **Cycles** (private) - Human-gated engineering loop.
  Flowtive tasks flow through Flowtive MCP and OpenClaw to an Engineer that runs every 10 minutes and implements through OpenCode ACP. A Reviewer runs every 15 minutes to gate PRs and route rework back to Flowtive.

```mermaid
flowchart TB
    F[Flowtive task] --> M[Flowtive MCP]
    M --> O[OpenClaw and Cycles]
    O --> ED[Engineer discovery\nselect eligible task\nevery 10 minutes]
    ED --> E[Engineer]
    E --> A[OpenCode via ACP]
    A --> P[Pull request]

    O --> RD[Reviewer discovery\nPR work first\nevery 15 minutes]
    P --> RD
    RD -->|PR ready| R[Review PR and task evidence]
    R -->|Pass| H[Human merge approval]
    R -->|Rework| F
    RD -->|No PR and scan due| I[Read-only risk scan\nmax once per 4 hours per project]
    I --> RF[Reviewer finding]
    RF --> F

    O -. Planned .-> TD[Tester discovery\nPR awaiting verification\ncoming soon]
    P -. PR awaits testing .-> TD
    TD -. Planned .-> T[Tester verification\ntest, lint, typecheck, build\ncoming soon]
    T -. Pass .-> R
    T -. Fail .-> F
```

The Tester path is planned but not active yet. It will verify PR-ready branches and
record evidence before work proceeds to review or returns for rework.

- [**openclaw-migrate**](https://github.com/programmerlapar/openclaw-migrate) - Cross-platform CLI that safely exports, inspects, restores, and rolls back OpenClaw agent environments.
- [**Atlas Photo**](https://github.com/programmerlapar/atlas-photo) - Privacy-first Electron photo application with local EXIF/GPS processing, interactive maps, thumbnail caching, and cross-platform packaging.

## Product And Platform Experience

- Full-stack product development with React, Next.js, TypeScript, and Node.js
- Serverless architecture with AWS Amplify Gen 2, Cognito, DynamoDB, S3, Lambda, and GraphQL
- AI workflows and developer tooling with Gemini, MCP, and agent orchestration
- Cross-platform desktop applications with Electron, Vite, and local-first data handling
- Product UX with Tailwind CSS, shadcn/ui, Radix UI, and accessible component systems

## Working With Me

I value reliable systems, clear product thinking, and practical automation. My public repositories show the tools and products I actively build.
