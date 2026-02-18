# 🛡️ Prowler Dashboard

Self-hosted Prowler App for cloud security assessments with web-based dashboard.

## 🚀 Quick Start

```bash
# Clone repo
git clone https://github.com/vanhoangkha/prowler-dashboard.git
cd prowler-dashboard

# Start services
docker compose up -d

# Access dashboard
open http://localhost:3000
```

## 📋 Requirements

- Docker & Docker Compose
- 4GB+ RAM recommended
- AWS/GCP/Azure credentials configured

## 🔧 Services

| Service | Port | Description |
|---------|------|-------------|
| **Prowler UI** | 3000 | Web dashboard |
| **Prowler API** | 8080 | REST API |
| **PostgreSQL** | 5432 | Database |
| **Valkey** | 6379 | Cache (Redis-compatible) |

## 📖 Usage

### 1. Access Dashboard
Navigate to http://localhost:3000 and sign up with email/password.

### 2. Add Cloud Provider
- Go to Settings → Providers
- Add AWS/GCP/Azure credentials
- Configure scan schedule

### 3. Run Scan
- Select provider and regions
- Choose compliance frameworks (CIS, NIST, HIPAA, etc.)
- Start scan and view results

### 4. API Documentation
Access API docs at http://localhost:8080/api/v1/docs

## ⚙️ Configuration

Edit `.env` file to customize:

```env
# Prowler versions
PROWLER_UI_VERSION="5.18.3"
PROWLER_API_VERSION="5.18.3"

# Database
POSTGRES_USER=prowler
POSTGRES_PASSWORD=prowler
POSTGRES_DB=prowler

# API settings
DJANGO_SECRET_KEY=your-secret-key
```

## 🔄 Update

```bash
# Pull latest images
docker compose pull --policy always

# Restart services
docker compose up -d
```

## 🛠️ Troubleshooting

```bash
# Check logs
docker compose logs -f

# Restart services
docker compose restart

# Reset (WARNING: deletes data)
docker compose down -v
docker compose up -d
```

## 📚 Resources

- [Prowler Documentation](https://docs.prowler.com)
- [Prowler GitHub](https://github.com/prowler-cloud/prowler)
- [Prowler Hub](https://hub.prowler.com)

## 📄 License

Apache 2.0 - See [Prowler License](https://github.com/prowler-cloud/prowler/blob/master/LICENSE)
