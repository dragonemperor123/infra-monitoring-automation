# Infrastructure Monitoring Automation

This project sets up an automated monitoring stack using **Prometheus**, **Grafana**, and **Node Exporter**, orchestrated with **Docker Compose**.  
It’s a simplified adaptation of the [vegasbrianc/prometheus](https://github.com/vegasbrianc/prometheus) project, customized to focus on **observability**, **automation**, and **SRE fundamentals** in a local environment.

---

## 💡 Overview

This setup demonstrates how to monitor infrastructure metrics such as CPU, memory, and disk usage across containers or hosts.  
Prometheus collects and stores time-series metrics, while Grafana visualizes them in dashboards. Node Exporter gathers host-level system metrics.

The project provides a practical introduction to:
- **Monitoring and observability pipelines**  
- **Alert rule configuration in Prometheus**  
- **Automated deployment using Docker Compose**  
- **SRE principles: availability, scalability, and reliability**

---

## ⚙️ Tech Stack

| Component | Purpose |
|------------|----------|
| **Prometheus** | Metric collection, querying, and alerting |
| **Grafana** | Dashboard visualization and analytics |
| **Node Exporter** | Host-level metric collection |
| **Docker Compose** | Container orchestration for simplified setup |

---

## 🧩 Architecture

```plaintext
+------------------+     +------------------+
|  Node Exporter   | --> |   Prometheus     |
|  (System Metrics)|     | (Scrape & Store) |
+------------------+     +------------------+
                               |
                               v
                        +------------------+
                        |     Grafana      |
                        | (Visualization)  |
                        +------------------+
