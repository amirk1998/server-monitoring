# Monitoring Stack with Prometheus, Grafana, and cAdvisor

This repository contains a Docker Compose setup for a comprehensive monitoring stack using Prometheus, Grafana, cAdvisor, and Node Exporter.

## Components

- **Prometheus**: A monitoring system and time series database.
- **Grafana**: A platform for monitoring and observability.
- **cAdvisor**: Provides resource usage and performance characteristics of running containers.
- **Node Exporter**: Exposes a wide variety of hardware and kernel-related metrics.

## Prerequisites

- Docker
- Docker Compose

## Setup

1. Clone this repository:
```bash
   git clone https://github.com/your-username/monitoring-stack.git
   cd monitoring-stack
```

2. Copy the `.env.example` file to `.env` and adjust the values as needed:
   ```bash
   cp .env.example .env
   ```
3. Modify the `.env` file to set your desired ports and Grafana admin credentials.

4. Start the monitoring stack:
   ```
   docker-compose up -d
   ```

5. Access the services:
   - Grafana: `http://localhost:<GRAFANA_PORT>`
   - Prometheus: `http://localhost:<PROMETHEUS_PORT>`
   - cAdvisor: `http://localhost:<CADVISOR_PORT>`
   - Node Exporter: `http://localhost:<NODE_EXPORTER_PORT>`

## Configuration

- Prometheus configuration is in `prometheus.yml`
- Grafana datasources are configured in `datasources.yml`
- Grafana dashboards can be added to the `dashboards` directory

## Security Considerations

- All sensitive information is stored in the `.env` file, which is not committed to the repository.
- Ensure to use strong passwords for Grafana admin access.
- Consider implementing additional security measures such as reverse proxy with HTTPS and authentication for Prometheus and cAdvisor.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.