# Kubrick web UI

This README was rewritten for the modified derivative repository; see the root [NOTICE](../../NOTICE) for attribution.

React and Vite chat interface for uploading videos and talking to the Kubrick agent. The Docker image builds the static UI and serves it with Nginx.

## Local development

```bash
npm ci
npm run dev
```

The development UI expects the API at `http://localhost:8080`. To run the complete application, follow the repository root [README](../README.md).

For public deployment, configure the UI API origin or route API requests through a same-origin reverse proxy; see the deployment note in the root README.
