# Cloud Monitoring and Alerting System

## Project Overview

This project implements a cloud-based monitoring and alerting system for an AWS EC2 instance. The system collects infrastructure metrics and provides real-time visualization and alerting.

## Technologies Used

- AWS EC2
- Docker
- Prometheus
- Node Exporter
- Grafana
- SMTP Email Alerting

## Architecture

AWS EC2 Instance
        |
        +-- Node Exporter
        |       |
        |       +-- System Metrics
        |
        +-- Prometheus
        |       |
        |       +-- Metrics Collection
        |
        +-- Grafana
                |
                +-- Dashboards
                +-- Alert Rules
                +-- Email Notifications

## Project Components

### Node Exporter

Node Exporter collects system-level metrics such as CPU, memory, disk and other infrastructure statistics from the EC2 instance.

### Prometheus

Prometheus collects metrics from Node Exporter at a configured interval.

The project uses a 15-second scrape interval.

### Grafana

Grafana is used to visualize the collected metrics through monitoring dashboards.



Grafana alert rules are configured to monitor infrastructure conditions and generate notifications when defined thresholds are reached.


The monitoring stack is deployed on an AWS EC2 Ubuntu instance using Docker containers.

## Docker Containers

The following containers are used:

- Prometheus
- Node Exporter
- Grafana


Prometheus configuration is available in:

`prometheus/prometheus.yml`


Project screenshots demonstrating the deployment, monitoring dashboard, Prometheus targets, and alerting configuration are included in the `screenshots` directory.


The project provides centralized infrastructure monitoring, visualization, and alert notifications for an AWS EC2 environment.


This project demonstrates the implementation of a containerized cloud monitoring solution using AWS EC2, Docker, Prometheus, Node Exporter, and Grafana.