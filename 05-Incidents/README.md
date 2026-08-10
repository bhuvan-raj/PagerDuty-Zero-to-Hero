# PagerDuty Incidents

## What is an Incident?

An incident represents an event that requires attention from an engineer.

An incident can be created when an alert is triggered by a monitoring or alerting system.

## Incident Lifecycle

```text
Triggered
    ↓
Acknowledged
    ↓
Resolved
```

### Triggered

The alert has created an incident and the assigned responder needs to investigate it.

### Acknowledged

The responder has accepted the incident and is working on the issue.

### Resolved

The issue has been fixed and the incident is closed.

## What You Will Learn

- What is an Incident?
- Incident lifecycle
- Triggering incidents
- Acknowledging incidents
- Resolving incidents
- Assigning incidents
- Reassigning incidents
- Incident escalation
- Incident timeline

## Practical

Trigger an incident and perform the complete lifecycle:

```text
Trigger
   ↓
Acknowledge
   ↓
Investigate
   ↓
Resolve
```

Also test what happens when the incident is not acknowledged within the configured escalation time.
