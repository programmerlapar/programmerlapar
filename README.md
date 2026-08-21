# Firmansyah Otoluwa

## Full-Stack Product Engineer | Agentic AI Systems

I build production web, mobile, and desktop products, plus engineering systems where AI agents implement and review software under human control.

**React** · **React Native** · **Expo** · **Next.js** · **TypeScript** · **Node.js** · **AWS Amplify Gen 2** · **Electron** · **MCP**

Open to remote full-stack, React Native/Expo, product engineering, and AI-agent platform opportunities.

## Selected Work

- **Cycles** (private) - Autonomous engineering orchestration connecting Flowtive, Flowtive MCP, OpenClaw, OpenCode ACP, GitHub pull requests, and human review. An Engineer claims and implements work; an independent Reviewer gates PRs and routes rework back to Flowtive.

- **Flowtive** (private source; public distribution) - Offline-first project management for Kanban, sprints, analytics, LAN sync, and AI-agent collaboration.
  - [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=kreaticode.flowtive) · [Open VSX](https://open-vsx.org/extension/kreaticode/flowtive) · [Chrome Web Store](https://chromewebstore.google.com/detail/flowtive-project-manageme/jlakbgpoiloflldfdjmjijafibgadno)
  - [Public releases and privacy policy](https://github.com/programmerlapar/flowtive-releases)

- [**Quidlass**](https://github.com/programmerlapar/quidlass) - Published React and TypeScript liquid-glass component library with zero runtime dependencies, 30+ configurable props, interactive effects, documentation, and a live demo.
  - [npm package](https://www.npmjs.com/package/quidlass) · [Documentation](https://programmerlapar.github.io/quidlass/) · [Live demo](https://programmerlapar.github.io/quidlass/demo/)

- [**Atlas Photo**](https://github.com/programmerlapar/atlas-photo) - Privacy-first Electron photo application with local EXIF/GPS processing, interactive maps, thumbnail caching, and cross-platform releases.
  - [Latest release](https://github.com/programmerlapar/atlas-photo/releases/latest)

- [**openclaw-migrate**](https://github.com/programmerlapar/openclaw-migrate) - Cross-platform TypeScript CLI for safely exporting, inspecting, restoring, and rolling back AI-agent environments.

## Engineering Evidence

- **Shipped products:** public marketplace listings, desktop releases, npm packages, live documentation, and demos
- **Full-stack delivery:** React, React Native/Expo, Next.js, TypeScript, Node.js, authentication, APIs, storage, payments, testing, and deployment
- **Serverless architecture:** AWS Amplify Gen 2, Cognito, DynamoDB, S3, Lambda, and GraphQL
- **AI-agent infrastructure:** MCP integrations, OpenClaw orchestration, ACP coding sessions, PR gates, and human-controlled delivery

<details>
<summary>View the Cycles architecture</summary>

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
    R -->|P2/P3 follow-up| F
    RD -->|No PR and scan due| I[Read-only risk scan\nmax once per 4 hours per project]:::reviewer
    I --> F[Reviewer finding or P2/P3 follow-up\nfiled in To Do]:::reviewer
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

Blue nodes are Engineer paths; purple nodes are Reviewer paths; muted, dashed nodes are the planned Tester path. The Tester role is not active yet.

</details>

## Contact

I am available for full-stack product development, React Native/Expo applications, serverless AWS work, and AI-agent engineering systems.
