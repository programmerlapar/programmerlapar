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
    B[Backlog column\nnot auto-claimed]:::column
    T[To Do column\nactive sprint]:::column
    IP[In Progress column]:::column
    RV[Review column]:::column
    RF[Review Failed column]:::column
    NR[Needs Rebase column]:::column
    TF[Test Failed column]:::column
    BL[Blocked column]:::column
    D[Done column]:::column

    B -. Human adds to sprint .-> T
    T --> M[Flowtive MCP]
    IP --> M
    RF --> M
    NR --> M
    TF --> M
    M --> O[OpenClaw and Cycles]

    O --> ED[Engineer discovery\nresume owned work or select eligible task\nevery 10 minutes]:::engineer
    ED -->|Eligible or rework| IP
    IP --> E[Engineer implementation]:::engineer
    E --> A[OpenCode via ACP]
    A --> P[Pull request]
    P --> RV
    E -->|Blocker| BL
    BL -. Human resolves .-> IP

    ED -->|No eligible task and improvement enabled| ID[Engineer improvement discovery\nrate-limited per project]:::engineer
    ID --> S[Suggestion column\nhuman promotes to To Do]:::column
    S -. Human promotion .-> T
    ED -->|No eligible task; no discovery due| EQ[Quiet exit]

    RV --> RD[Reviewer discovery\nPR work first\nevery 15 minutes]:::reviewer
    O --> RD
    RD -->|Reviewable PR| R[Review PR and task evidence]:::reviewer
    R -->|Pass| H[Human merge approval]
    H --> D
    R -->|P0/P1 findings| RF
    R -->|Merge conflict| NR
    RD -->|No PR and scan due| I[Read-only risk scan\nmax once per 4 hours per project]:::reviewer
    I --> F[Reviewer finding\nfiled in To Do]:::reviewer
    F --> T
    RD -->|No PR; scan not due| RQ[Quiet exit]

    P -. Planned testing path .-> TD[Tester discovery\nPR awaiting verification\ncoming soon]:::tester
    TD -. Planned .-> TV[Tester verification\ntest, lint, typecheck, build\ncoming soon]:::tester
    TV -. Pass .-> RV
    TV -. Fail .-> TF

    classDef column fill:#f8fafc,stroke:#64748b,color:#334155;
    classDef engineer fill:#dbeafe,stroke:#2563eb,color:#1e3a8a;
    classDef reviewer fill:#f3e8ff,stroke:#9333ea,color:#581c87;
    classDef tester fill:#f8fafc,stroke:#94a3b8,stroke-dasharray: 5 5,color:#64748b;
```

Blue nodes are Engineer paths; purple nodes are Reviewer paths; muted, dashed nodes
are the planned Tester path. Backlog tasks are intentionally excluded until a human
adds them to an active sprint. The Tester role is not active yet; it will verify
PR-ready branches and record evidence before work proceeds to review or rework.

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
