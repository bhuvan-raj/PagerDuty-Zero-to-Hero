# Real-World PagerDuty Incident Management Lab

## Objective

Build a complete monitoring and incident-management workflow using Prometheus, Grafana, and PagerDuty.

## Architecture

```text
                    ┌──────────────┐
                    │ Application  │
                    └──────┬───────┘
                           ↓
                    ┌──────────────┐
                    │  Prometheus  │
                    └──────┬───────┘
                           ↓
                    ┌──────────────┐
                    │   Grafana    │
                    │   Alerting   │
                    └──────┬───────┘
                           ↓
                    ┌──────────────┐
                    │  PagerDuty   │
                    └──────┬───────┘
                           ↓
                    ┌──────────────┐
                    │   Service    │
                    └──────┬───────┘
                           ↓
                  ┌──────────────────┐
                  │ Escalation Policy│
                  └────────┬─────────┘
                           ↓
                    ┌──────────────┐
                    │  On-Call     │
                    │  Engineer    │
                    └──────────────┘
```

## Prerequisites

- Kubernetes cluster
- Prometheus
- Grafana
- PagerDuty account
- Basic understanding of monitoring and alerting

## Lab Tasks

### 1. Configure Monitoring

Deploy or configure Prometheus and Grafana.

Verify that Grafana is receiving metrics from Prometheus.

### 2. Create PagerDuty Users

Create the users who will participate in the on-call rotation.

### 3. Create an On-Call Schedule

Create a schedule with a primary and secondary responder.

```text
Primary
   ↓
Secondary
```

### 4. Create an Escalation Policy

Configure:

```text
Level 1 → Primary On-Call
Level 2 → Secondary On-Call
```

Configure an escalation timeout.

### 5. Create a PagerDuty Service

Create a service for the application.

Connect the service to the escalation policy.

### 6. Configure Grafana Alerting

Create an alert rule.

Example:

```text
CPU Usage > 80%
```

Configure Grafana to send the alert to PagerDuty.

### 7. Trigger the Alert

Generate the required condition so that the Grafana alert enters the firing state.

Expected flow:

```text
Metric Threshold Exceeded
          ↓
    Grafana Alert
          ↓
       PagerDuty
          ↓
       Incident
```

### 8. Acknowledge the Incident

Verify that the assigned on-call engineer receives the notification.

Acknowledge the incident.

Expected:

```text
Triggered
    ↓
Acknowledged
```

### 9. Resolve the Incident

Fix the condition that caused the alert.

Resolve the PagerDuty incident.

Expected:

```text
Acknowledged
     ↓
Resolved
```

### 10. Test Escalation

Trigger the alert again.

This time, do not acknowledge the incident.

Verify:

```text
Incident
   ↓
Primary On-Call
   ↓
Timeout
   ↓
Secondary On-Call
```

## Expected Outcome

After completing this lab, you should be able to demonstrate a complete production-style incident workflow:

```text
Monitoring
    ↓
Metrics
    ↓
Grafana Alert
    ↓
PagerDuty Incident
    ↓
On-Call Notification
    ↓
Escalation
    ↓
Acknowledgement
    ↓
Resolution
```

## Final Objective

The goal of this lab is to understand how a monitoring alert is converted into an actionable production incident and routed to the correct engineer through PagerDuty.
