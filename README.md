# Project name

> One-sentence description of what your system does and for whom.

## Authors

| Name         | GitHub       | Main responsibilities |
|--------------|--------------|-----------------------|
| Gregor Gegič | @gegicgregor | Mobile app, Database  |
| Jaša Žabkar  | @Asaj79      | Web front end, API    |

<!-- Lab repository: one row. Project repository: both team members. -->

## Live system

| Part | URL |
|------|-----|
| Web app | … |
| API (+ docs) | … |
| Health check | … |
| Mobile app | build instructions below / APK in Releases |

## Architecture

See [docs/architecture.md](docs/architecture.md).

```mermaid
flowchart LR
    Web[Web app] --> API
    Mobile[Mobile app] --> API
    Agent[AI agent] --> API
    API --> DB[(Database)]
    API --> LLM[LLM provider]
```

## Stack

| Part | Technology |
|------|------------|
| Backend | FastAPI |
| Web front end | Rest |
| Database | PostgreSQL |
| Mobile | Rest Native |
| Cloud  | tba |
| LLM provider | tba |

Reasons: see [docs/decisions/](docs/decisions/).

## Running locally

### Prerequisites
- …

### Configuration (secrets)
Describe which environment variables / user secrets are needed and how to set them.
**Never commit real secrets.**

### Start
```bash
# e.g. docker compose up
```

### Tests
```bash
# e.g. dotnet test / npm test / pytest
```

### Mobile app
How to build and run it, and how to point it to a local or production API.

## Documentation

| Document | Content |
|----------|---------|
| [docs/proposal.md](docs/proposal.md) | Problem, users, user stories |
| [docs/data-model.md](docs/data-model.md) | ER diagram |
| [docs/architecture.md](docs/architecture.md) | Components and deployment |
| [docs/api/openapi.yaml](docs/api/openapi.yaml) | REST API contract |
| [docs/agent.md](docs/agent.md) | Agent tools and guardrails |
| [docs/decisions/](docs/decisions/) | Architecture decision records |
| [docs/ai-usage-log.md](docs/ai-usage-log.md) | How we used AI tools |
