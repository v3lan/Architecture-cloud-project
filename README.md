# Cloud Infrastructure Deployment & Monitoring Capstone

## 📌 Project Overview
An end-to-end containerized Node.js application deployed behind an Nginx reverse proxy with automated CI/CD via GitHub Actions and Prometheus monitoring integration.

---

## 🏗️ Architecture & Stack
- **Backend:** Node.js (Express framework)
- **Database:** PostgreSQL containerized instance
- **Reverse Proxy:** Nginx (Rate limiting, Gzip, SSL termination)
- **Containerization:** Multi-stage Docker build & Docker Compose orchestration
- **CI/CD:** GitHub Actions (Automated linting, testing, image build)
- **Monitoring:** Prometheus uptime & health check scraping (`/health`)

---

## 🚀 Cloud Deployment Instructions (AWS EC2 / DigitalOcean)

### 1. Provision Infrastructure & Server Setup
```bash
# Clone the repository
git clone https://github.com/v3lan/Architecture-cloud-project.git
cd cloud-architecture-project

# Configure environment variables
cat <<EOF> .env
PORT=3000
DATABASE_URL=postgres://postgres:postgres@db:5432/appdb
EOF
