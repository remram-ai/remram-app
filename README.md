# remram-app

User-facing surface for the Remram system.

`remram-app` contains the API layer, web application, and future mobile interfaces that connect users to the Remram runtime and Cortex memory service.

This repository is responsible for presentation and client interaction. It does not execute agents or manage memory directly.

---

## Purpose

`remram-app` provides:

- Public and internal API endpoints
- Web application UI
- Authentication and user session management
- Client-side interaction with agents
- Structured access to Cortex knowledge

The app connects to the Remram runtime (`remram-gateway`) and Cortex (`remram-cortex`) through defined service interfaces.

---

## Project Structure (Application Layout)

The exact framework may evolve, but the structure will follow a standard service + client separation.

```
remram-app/
  README.md

  api/
    server/
    routes/
    middleware/

  web/
    src/
    public/

  mobile/           # Future mobile client

  shared/
    types/
    client/

  config/
```

### `api/`

Backend service layer.

- Handles authentication
- Proxies or aggregates requests to Gateway and Cortex
- Enforces user-level access controls

### `web/`

Primary browser-based application.

- UI components
- Agent interaction views
- Memory visualization
- Knowledge browsing interfaces

### `mobile/`

Reserved for future native or hybrid mobile clients.

### `shared/`

Shared types, API clients, and cross-surface utilities.

---

## Responsibility Boundary

`remram-app` is a client and API surface.

It does not:

- Define agents
- Execute tools
- Perform memory indexing
- Manage runtime orchestration

It connects users to the Remram system.

---

## Relationship to Other Repositories

- `remram-gateway` — Execution runtime
- `remram-agents` — Agent definitions
- `remram-cortex` — Knowledge authority
- `remram` — System documentation

The app presents. The runtime executes. Cortex remembers.

