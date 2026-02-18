# Prowler Dashboard

[![Docker](https://img.shields.io/badge/docker-ready-blue)](https://docker.com)

Prowler security findings dashboard with PostgreSQL and Valkey.

## Architecture

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│   Prowler   │────▶│  PostgreSQL │◀────│  Dashboard  │
│   Scanner   │     │   Database  │     │     UI      │
└─────────────┘     └─────────────┘     └─────────────┘
                           │
                    ┌──────┴──────┐
                    │   Valkey    │
                    │   (Cache)   │
                    └─────────────┘
```

## Quick Start

```bash
# Configure
cp .env.example .env
# Edit .env with your settings

# Start
docker-compose up -d

# View logs
docker-compose logs -f
```

## Configuration

See `.env` file for all configuration options.

## License

MIT
