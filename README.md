# Neuron Network

Learning project: build the smallest end-to-end neural-network app with a web UI and a C# backend.

This repository starts with **documentation first** (no code yet).

## Target stack (decisions)

### Backend
- **ASP.NET Core Web API** on **.NET 10**
- IDE: **Visual Studio**

### REST testing (chosen)
- **Swagger UI** (OpenAPI) in the browser

### Frontend (UI)
- **React**
- IDE: **Visual Studio Code** (later)

## API style
- Endpoints use **lowercase** paths (example: `/predict`, `/train`).

## Minimal architecture (Phase 1)
- Backend exposes `POST /predict`
- Phase 1: `/predict` returns a placeholder value (dummy “model”)
- Swagger is used to test `/predict` during backend development
- React UI will be added later and will call the same endpoint

## Phases / milestones

### Phase 0 — Documentation ✅
- [x] Define repository structure
- [x] Define API contract (`/predict`, later `/train`)
- [x] Define dev workflow (VS + Swagger; later VS Code for React)

### Phase 1 — Web API + Swagger testing (no neural net yet) ← *current*
- [ ] Create ASP.NET Core Web API project (`Neuron.Api`) targeting **.NET 10**
- [ ] Add endpoint: `POST /predict`
- [ ] Verify request/response in Swagger UI
- [ ] Confirm API contract is stable

### Phase 2 — First real neural net (XOR)
- [ ] Add `POST /train`
- [ ] Make `/predict` use trained weights (in-memory to start)
- [ ] Test `/train` and `/predict` via Swagger

### Phase 3 — UI (optional)
- [ ] React UI calls the same API endpoints

## Proposed repository structure
- `docs/`
  - `docs_api_Version_1.md` (API contract)
  - `docs_dev-workflow_Version_1.md` (how to run and test)
  - `docs_routing_Version_1.md` (routing conventions: lowercase)
  - `docs_glossary_Version_1.md` (terms)
- `Neuron.Api/` (later: Visual Studio Web API project)
- `neuron-web/` (later: React UI)