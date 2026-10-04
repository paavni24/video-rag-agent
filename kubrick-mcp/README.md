# Kubrick MCP server

This README was rewritten for the modified derivative repository; see the root [NOTICE](../../NOTICE) for attribution.

FastMCP service that indexes video/audio and provides tools, resources, and prompts to the Kubrick agent API. In the full application, Compose connects it to `kubrick-api` and `kubrick-ui`.

## Configuration

From the repository root, copy `kubrick-mcp/.env.example` to `kubrick-mcp/.env` and set `OPENAI_API_KEY`, `OPIK_API_KEY`, `OPIK_WORKSPACE`, and `OPIK_PROJECT`. These credentials are required for video processing and Opik prompt management. Never commit `.env`.

## Run as part of the application

Follow the repository root [README](../README.md) to configure and start the full Compose stack. The MCP endpoint is `http://localhost:9090/mcp`; use an MCP client or inspector to interact with it.

For Python development, install dependencies with `uv sync --frozen` from this directory. Video indexes are stored in Pixeltable; the Compose setup persists them in a Docker volume.
