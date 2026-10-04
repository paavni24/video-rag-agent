# Kubrick API

This README was rewritten for the modified derivative repository; see the root [NOTICE](../../NOTICE) for attribution.

FastAPI service for chat, video upload and processing, agent memory, and serving generated clips. In the full application, Docker Compose connects this service to `kubrick-mcp` and `kubrick-ui`.

## Configuration

From the repository root, copy `kubrick-api/.env.example` to `kubrick-api/.env` and set `GROQ_API_KEY`. Opik settings are optional for API-side tracing. Never commit `.env`.

## Run as part of the application

Follow the repository root [README](../README.md) to create all environment files and start the full Compose stack. API docs are available locally at <http://localhost:8080/docs>.

For Python development, install dependencies with `uv sync --frozen` from this directory. The API expects the MCP service at `http://kubrick-mcp:9090/mcp` when running in Compose.
