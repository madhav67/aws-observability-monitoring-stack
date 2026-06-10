# AWS Observability Stack using Prometheus, Grafana, Loki and Alloy

## Project Overview

This project demonstrates a complete observability platform built on AWS using Prometheus, Grafana, Loki, Alloy, and Node Exporter.

The objective was to build a centralized monitoring and logging solution capable of collecting:

- Infrastructure Metrics
- Application Metrics
- System Logs
- Alert Notifications

while providing real-time visualization through Grafana dashboards.

---

## Architecture

```text
                +----------------+
                |   Grafana      |
                | Dashboards     |
                | Alerting       |
                +--------+-------+
                         |
          +--------------+-------------+
          |                            |
          v                            v

+----------------+         +------------------+
| Prometheus     |         | Loki             |
| Metrics Store  |         | Log Aggregation  |
+--------+-------+         +---------+--------+
         |                           |
         |                           |
         v                           v

+----------------+         +------------------+
| Node Exporter  |         | Alloy            |
| System Metrics |         | Log Collection   |
+--------+-------+         +---------+--------+
         |                           |
         +-------------+-------------+
                       |
                       v

              +----------------+
              | Flask App      |
              | /metrics       |
              | Access Logs    |
              +----------------+

                       |
                       v

                 Slack Alerts
```

---

## Technologies Used

- AWS EC2
- Prometheus
- Grafana
- Loki
- Alloy
- Node Exporter
- Python Flask
- PromQL
- Slack Webhooks
- Linux

---

## Features Implemented

### Infrastructure Monitoring

Collected:

- CPU Utilization
- Memory Utilization
- Disk Usage
- Load Average
- Process Metrics

using Node Exporter.

---

### Application Monitoring

Instrumented a Flask application using Prometheus Python Client.

Exposed:

- HTTP Request Count
- Request Rate
- Endpoint Metrics
- Process Metrics
- Python GC Metrics
- Memory Metrics

through:

```text
/metrics
```

endpoint.

---

### Stress Testing

Generated artificial workload using:

```bash
stress-ng
```

to validate dashboard behavior and monitoring accuracy.

Simulated:

- CPU Load
- Memory Consumption
- Disk Activity

---

### Grafana Dashboards

Created custom dashboards using PromQL.

Panels included:

- CPU Utilization (%)
- Memory Availability (%)
- HTTP Requests per Second
- Request Counters
- Endpoint Specific Metrics
- Dynamic Dashboard Variables

---

### Alerting

Configured Grafana Alert Rules.

Integrated alerts with Slack.

Notifications were automatically sent when thresholds were exceeded.

---

### Centralized Logging

Configured Alloy and Loki for log aggregation.

Collected:

```text
/var/log/titan/access.log
```

Visualized:

- Log Volume
- Request Patterns
- Error Events
- Application Activity

inside Grafana Explore.

---

## Key Learning Outcomes

This project provided hands-on experience with:

- Observability Fundamentals
- Metrics Collection
- Prometheus Architecture
- PromQL Queries
- Grafana Dashboards
- Loki Log Aggregation
- Grafana Alloy
- Alerting Pipelines
- Slack Integrations
- AWS Infrastructure Monitoring
