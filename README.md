<div align="center">

<img src="https://www.pagerduty.com/wp-content/uploads/2023/06/pagerduty-logo.png" width="260" alt="PagerDuty" />

# PagerDuty — Zero to Hero 🚀

**A practical, real-world learning path for Incident Management with PagerDuty + Grafana Alerting**

[![PagerDuty](https://img.shields.io/badge/PagerDuty-06AC38?style=for-the-badge&logo=pagerduty&logoColor=white)](https://www.pagerduty.com/)
[![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)](https://grafana.com/)
[![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)](https://prometheus.io/)
[![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](#)

</div>

---

## 📖 About

**PagerDuty** is an incident management platform used by DevOps and SRE teams to manage alerts, incidents, on-call schedules, and escalation workflows.

This repository is a **Zero to Hero** learning path that walks through PagerDuty from the fundamentals to a full real-world integration with **Grafana Alerting** — the way it's actually used in production DevOps environments.

---

## 📚 Table of Contents

| # | Module | Description |
|:-:|--------|-------------|
| 01 | [Introduction to PagerDuty](./01-Introduction/README.md) | Core concepts and platform overview |
| 02 | [Services](./02-Services/README.md) | Configuring services and integrations |
| 03 | [On-Call Schedules](./03-On-Call-Schedules/README.md) | Building rotations and coverage |
| 04 | [Escalation Policies](./04-Escalation-Policies/README.md) | Routing alerts to the right people |
| 05 | [Incidents](./05-Incidents/README.md) | Lifecycle: trigger, acknowledge, resolve |
| 06 | [Grafana → PagerDuty Integration](./06-Grafana-PagerDuty-Integration/README.md) | Connecting alert rules to PagerDuty |
| 07 | [Real-World Incident Management Lab](./07-Real-World-Lab/README.md) | End-to-end hands-on scenario |

---

## 🔄 Workflow Overview

```text
Application / Kubernetes
        │
        ▼
   Prometheus
        │
        ▼
    Grafana
        │
        ▼
  Alert Rule
        │
        ▼
   PagerDuty
        │
        ▼
    Service
        │
        ▼
Escalation Policy
        │
        ▼
On-Call Engineer
        │
        ▼
    Incident
        │
        ▼
Acknowledge / Resolve
```

**Prometheus** collects metrics → **Grafana** evaluates alert rules → **PagerDuty** handles incident routing, on-call escalation, and resolution.

---

## 🏗️ Final Architecture

```text
┌──────────────┐
│ Application  │
└──────┬───────┘
       ▼
┌──────────────┐
│  Prometheus  │
└──────┬───────┘
       ▼
┌──────────────┐
│   Grafana    │
│   Alerting   │
└──────┬───────┘
       ▼
┌──────────────┐
│  PagerDuty   │
└──────┬───────┘
       ▼
┌──────────────┐
│   Service    │
└──────┬───────┘
       ▼
┌────────────────────┐
│ Escalation Policy   │
└──────────┬──────────┘
       ▼
┌──────────────┐
│   On-Call    │
│   Engineer   │
└──────┬───────┘
       ▼
┌──────────────┐
│   Incident   │
└──────────────┘
```

---

## 🎯 Goal

By completing this repository, you'll be able to configure PagerDuty for a real-world DevOps monitoring workflow — routing alerts from Grafana through PagerDuty **services**, **on-call schedules**, and **escalation policies**, all the way to a fully managed **incident**.

---

## 🛠️ Prerequisites

- A [PagerDuty](https://www.pagerduty.com/sign-up/) account (free trial works)
- A running [Grafana](https://grafana.com/) instance with alerting enabled
- Basic familiarity with Prometheus metrics and alert rules

---

## 🤝 Contributing

Contributions, corrections, and suggestions are welcome — feel free to open an issue or a pull request.

---

<div align="center">

**⭐ If this repository helped you, consider giving it a star!**

</div>
