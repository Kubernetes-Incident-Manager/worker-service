# Worker Service

## Overview
The **Worker Service** processes asynchronous background tasks and jobs outside of the main HTTP request cycle. It is primarily used for handling long-running operations, sending external notifications (e.g., Slack, Email), and processing message queues (e.g., Azure Service Bus).

## Features
- Listens to message queues or service bus topics.
- Sends Slack, Email, or SMS notifications when incidents occur or change status.
- Processes heavy data transformations or synchronization jobs asynchronously.
- Built with Python.

## Getting Started

### Prerequisites
- Python 3.10+
- `pip` package manager
- Docker (optional for containerized deployment)
- Azure Service Bus / Message Queue access (as configured in `.env`)

### Installation
1. Navigate to the service directory:
   ```bash
   cd services/worker-service
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Running the Service
To run the service locally for development:
```bash
python app/main.py
```

## Docker
Build the Docker image:
```bash
docker build -t incident-tracker/worker-service .
```
Run the Docker container:
```bash
docker run incident-tracker/worker-service
```
