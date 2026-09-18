# ☁️ Cloud Monitoring and Alerting System

A cloud-based monitoring and alerting system built to monitor an **AWS EC2 instance** using **Prometheus, Node Exporter, Grafana, and Docker**.

The project collects infrastructure metrics, visualizes them through Grafana dashboards, and provides alert notifications when configured conditions are reached.

## 🚀 Project Overview

This project implements a containerized monitoring solution for an AWS EC2 Ubuntu instance.

The system collects important infrastructure metrics such as:

* CPU usage
* Memory usage
* Disk usage
* System-level metrics

These metrics are collected using **Node Exporter and Prometheus**, visualized using **Grafana**, and monitored using Grafana alert rules.

## 🛠️ Technologies Used

* **AWS EC2** – Cloud server infrastructure
* **Docker** – Containerization
* **Prometheus** – Metrics collection and monitoring
* **Node Exporter** – System metrics collection
* **Grafana** – Monitoring dashboards and alerting
* **SMTP** – Email notifications
* **Ubuntu** – Operating system

## 🏗️ Architecture

```text
                    AWS EC2 - Ubuntu
                           │
                           ▼
                    ┌──────────────┐
                    │ Node Exporter│
                    └──────┬───────┘
                           │
                    System Metrics
                           │
                           ▼
                    ┌──────────────┐
                    │  Prometheus  │
                    └──────┬───────┘
                           │
                     Metrics Data
                           │
                           ▼
                    ┌──────────────┐
                    │   Grafana    │
                    └──────┬───────┘
                           │
                    ┌──────┴───────┐
                    │              │
                Dashboards     Alert Rules
                                   │
                                   ▼
                             Email Alerts
```

## 🔧 Project Components

### 1. Node Exporter

Node Exporter collects system-level metrics from the EC2 instance.

It provides metrics related to:

* CPU
* Memory
* Disk
* Network
* System performance

### 2. Prometheus

Prometheus collects and stores metrics from Node Exporter.

The project uses a **15-second scrape interval** to periodically collect the metrics.

Prometheus configuration is available in:

```text
prometheus/prometheus.yml
```

### 3. Grafana

Grafana is used to visualize the metrics collected by Prometheus.

The project includes monitoring dashboards for observing the infrastructure and Grafana alert rules for monitoring configured conditions.

### 4. Docker

The monitoring stack runs using Docker containers.

The project uses containers for:

* Prometheus
* Node Exporter
* Grafana

This makes the monitoring components easier to deploy and manage.

### 5. Email Alerting

SMTP email notification is configured for sending alerts when defined monitoring conditions are reached.

## 🔄 How It Works

```text
EC2 Instance
     ↓
Node Exporter
     ↓
Prometheus
     ↓
Grafana
     ↓
Dashboards + Alert Rules
     ↓
Email Notification
```

## 📊 Monitoring Flow

1. An AWS EC2 Ubuntu instance runs the monitoring stack.
2. Node Exporter collects system metrics.
3. Prometheus periodically scrapes the metrics.
4. Prometheus stores the collected metrics.
5. Grafana connects to Prometheus.
6. Grafana displays the metrics using dashboards.
7. Alert rules monitor configured conditions.
8. Email notifications are generated when alert conditions are reached.

## 📁 Project Structure

```text
Cloud_Monitoring_Project/
│
├── prometheus/
│   └── prometheus.yml
│
├── screenshots/
│
├── grafana/
│
├── docker-compose.yml
│
└── README.md
```

> The exact project structure may vary depending on the files included in the repository.

## 🎯 Key Features

* ☁️ AWS EC2 infrastructure monitoring
* 📊 Real-time metric visualization
* 🖥️ CPU, memory, disk and system monitoring
* 🔍 Prometheus metric collection
* 📈 Grafana dashboards
* 🚨 Grafana alert rules
* 📧 Email notifications
* 🐳 Docker-based deployment
* ⚙️ 15-second Prometheus scrape interval

## 🎓 What I Learned

Through this project, I gained practical experience with:

* AWS EC2
* Docker and containerized applications
* Prometheus
* Node Exporter
* Grafana
* Infrastructure monitoring
* Metrics collection
* Monitoring dashboards
* Alert configuration
* SMTP email notifications
* Linux/Ubuntu server administration

## 🔮 Future Improvements

Possible improvements include:

* Adding more infrastructure metrics
* Monitoring multiple EC2 instances
* Adding centralized logging
* Implementing automated deployment using CI/CD
* Adding more advanced Grafana dashboards
* Integrating additional notification channels
* Deploying the monitoring stack using infrastructure-as-code tools such as Terraform

## 👨‍💻 Author

**Praneeth Vakamullu**

GitHub: [@praneeth1093](https://github.com/praneeth1093)
