# ELK Stack on Docker

## Overview

This project sets up an ELK (Elasticsearch, Logstash, Kibana) stack with Prometheus and Grafana using Docker-Compose.

## Services

- **Elasticsearch Master** (1 node)
- **Elasticsearch Data Nodes** (2 nodes, scalable)
- **Kibana** (Visualization UI)
- **Logstash** (Data processing pipeline)
- **Prometheus** (Metrics monitoring)
- **Grafana** (Dashboard for visualization)

## Setup Instructions

### Prerequisites

- Docker and Docker Compose installed

### Run the Stack

1. Clone the repository:

   ```sh
   git clone https://github.com/your-repo/elk.git
   cd ELK
   ```
2. Ensure all configuration files in `./config/` are correctly set up.
3. Start the stack:

   ```sh
   docker-compose up -d
   ```
4. Check the running services:

   ```sh
   docker ps
   ```

### Stopping the Stack

To stop all services:

```sh
docker-compose down
```

### Scaling Data Nodes

To add more data nodes, modify the `docker-compose.yml` file by duplicating a data node service and changing its name and volume mapping.

## Accessing Services

- **Elasticsearch**: `http://localhost:9200`
- **Kibana**: `http://localhost:5601`
- **Logstash**: `http://localhost:5044`
- **Prometheus**: `http://localhost:9090`
- **Grafana**: `http://localhost:3000`

## Configuration

All configurations are stored in the `./config/` directory. Modify them as needed before running the stack.
