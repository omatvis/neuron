# Routing conventions (lowercase endpoints)

Decision: the API uses **lowercase** endpoint paths:

- `/predict`
- `/train`

## Why
- Common REST style in documentation and examples
- Easy to type and consistent across platforms
- Avoids mixing casing styles between controllers and routes

## Implications for ASP.NET Core
ASP.NET Core can generate routes in different ways depending on how endpoints are mapped.

To keep paths lowercase, we will **explicitly set routes** (instead of relying on default controller naming that can result in `/Predict`).

## Rules for this repo
- Public HTTP paths are lowercase.
- Do not expose mixed-case routes (avoid both `/Predict` and `/predict` existing at the same time).
- Swagger should show lowercase paths.

## Notes (implementation later)
When we implement controllers, we will:
- set route templates explicitly (example idea: `[Route("predict")]`)
- keep action methods consistent with the contract in `docs/api.md`