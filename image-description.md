## 01 - AWS Infrastructure

Four EC2 instances hosting Prometheus, Grafana, Loki and the Flask application.

---

## 02 - Flask Metrics Endpoint

Prometheus metrics exposed through the Flask /metrics endpoint.

Includes request counters, memory usage, process metrics and GC statistics.

---

## 03 - Node Exporter Metrics

System-level metrics exposed by Node Exporter.

---

## 04 - Stress Testing

Generated CPU, memory and disk load using stress-ng to validate monitoring.

---

## 05 - CPU Utilization Dashboard

Grafana dashboard visualizing CPU consumption using PromQL.

---

## 06 - Memory Availability Dashboard

Real-time memory monitoring panel with threshold visualization.

---

## 07 - HTTP Request Dashboard

Request traffic analysis per endpoint using Prometheus metrics.

---

## 08 - Dynamic Dashboard Variables

Grafana variables allowing endpoint-level filtering.

---

## 09 - Slack Alert Integration

Grafana alerts delivered automatically to Slack channels.

---


## 10 - Grafana Alloy Health

Alloy components configured for metrics and log collection.

---

## 11 - Monitoring Stack Overview

Complete monitoring platform showing metrics, logs, dashboards and alerts.