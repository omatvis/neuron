# Development workflow (planned)

## Backend (ASP.NET Core Web API, .NET 10) — Visual Studio
- Create and run the API project in Visual Studio.
- Use an HTTPS launch profile (local dev certificate).
- Keep Swagger/OpenAPI enabled.

## REST testing — Swagger UI (chosen)
- When the API is running locally, open Swagger UI:
  - `https://localhost:{PORT}/swagger`
- Use Swagger to manually call endpoints:
  - expand endpoint
  - click **Try it out**
  - send request JSON
  - review status code + response JSON

## Frontend (React) — Visual Studio Code (later)
- React dev server runs separately (Node.js + npm).
- The React UI will call the same endpoints already tested via Swagger.

## Integration notes (Phase 1+)
- React (HTTP) calling ASP.NET (HTTPS) may require:
  - CORS configuration on the backend
  - using the correct backend base URL + port
- Keep the API contract stable so UI changes are minimal later.