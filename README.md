# Grafana Research

Research and prototyping for Grafana AI-powered observability — focusing on a **Self-Correcting Query Assistant** concept.

## Overview

This repo contains a local reproduction environment for exploring Grafana Cloud integrations:

- **Prometheus** — local metrics collection
- **Grafana Alloy** — forwarding metrics to Grafana Cloud
- **Recording Rules** — pre-aggregated metrics via `rules.yml`

## Architecture

```
Prometheus (scrape) → Alloy (remote_write) → Grafana Cloud
```

## Quick Start

1. Copy `.env.example` to `.env` and fill in your Grafana Cloud credentials:
   ```bash
   cp .env.example .env
   ```

2. Start the stack:
   ```bash
   docker compose up -d
   ```

3. Access:
   - Prometheus UI: http://localhost:9090
   - Alloy UI: http://localhost:12345

## Project Context

Exploring how AI can improve the observability query experience — specifically a feedback-loop-driven self-correcting query assistant that learns from user corrections to improve future query suggestions.

## License

MIT
