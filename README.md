# Local Development Environment (AI generated)

This repository contains Docker Compose configurations for setting up a local development environment with various services including Kafka, PostgreSQL, and ClickHouse.

## Getting Started

1. Clone this repository
2. Navigate to the specific service directory you want to start
3. Run the following command:
   ```bash
   docker-compose up -d
   ```

## Service-Specific Instructions

### Kafka
```bash
cd docker/kafka
docker-compose up -d
```
Access AKHQ UI at http://localhost:9090

### PostgreSQL
```bash
cd docker/postgres
docker-compose up -d
```
Connect to the database using:
- Host: localhost
- Port: 5432
- Database: postgres
- Username: user
- Password: password

### ClickHouse
```bash
cd docker/clickhouse
docker-compose up -d
```
Access ClickHouse:
- Native protocol: localhost:9000
- HTTP interface: http://localhost:8123

## Notes

- All services are configured with `restart: unless-stopped` policy
- Services are isolated in their own networks
- Default configurations are suitable for local development
- For production use, please review and adjust security settings
