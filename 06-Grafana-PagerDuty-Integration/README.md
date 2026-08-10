# Grafana → PagerDuty Integration

## Overview

In this module, Grafana Alerting will be integrated with PagerDuty.

Prometheus will provide metrics to Grafana, Grafana will evaluate the alert rule, and PagerDuty will handle the resulting incident.

## Architecture

```text
Prometheus
    ↓
Metrics
    ↓
Grafana
    ↓
Alert Rule
    ↓
PagerDuty
    ↓
Service
    ↓
On-Call Engineer
```

## What You Will Learn

- Grafana Alerting
- Creating a Grafana Alert Rule
- PagerDuty integration
- PagerDuty integration key
- Configuring a notification/contact point
- Connecting Grafana to PagerDuty
- Triggering a PagerDuty incident from Grafana

## Practical

Create a Grafana alert for a monitored metric.

For example:

```text
CPU Usage > 80%
```

When the alert condition is met:

```text
Grafana Alert
     ↓
PagerDuty
     ↓
Incident
     ↓
On-Call Engineer
```

## Expected Result

When the Grafana alert is triggered:

1. Grafana detects the alert condition.
2. Grafana sends the alert to PagerDuty.
3. PagerDuty creates an incident.
4. The assigned on-call engineer is notified.
5. The engineer acknowledges the incident.
6. The engineer resolves the incident.
