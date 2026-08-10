# PagerDuty Services

## What is a Service?

A Service in PagerDuty represents an application, system, or component that needs to be monitored.

Alerts sent to a PagerDuty Service can create incidents and trigger the associated escalation policy.

## Service Workflow

```text
Monitoring Tool
      ↓
    Alert
      ↓
   Service
      ↓
Escalation Policy
```

## What You Will Learn

- What is a PagerDuty Service?
- Creating a Service
- Service configuration
- Connecting a Service to an Escalation Policy
- Service integrations
- Integration keys

## Practical

Create a PagerDuty Service that will receive alerts from Grafana.

```text
Grafana
   ↓
PagerDuty Service
```
