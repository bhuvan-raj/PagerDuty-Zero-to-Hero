# PagerDuty Escalation Policies

## What is an Escalation Policy?

An Escalation Policy defines who should be notified when an incident occurs and how the incident should be escalated if the current responder does not acknowledge it.

## Example

```text
Incident
   ↓
Primary On-Call
   ↓
No Acknowledgement
   ↓
Secondary On-Call
   ↓
No Acknowledgement
   ↓
Team Lead
```

## What You Will Learn

- What is an Escalation Policy?
- Creating an Escalation Policy
- Escalation levels
- Primary responder
- Secondary responder
- Escalation timeout
- Connecting escalation policies with services
- Connecting escalation policies with on-call schedules

## Practical

Create an escalation policy with:

```text
Level 1 → Primary On-Call
Level 2 → Secondary On-Call
```

Configure an escalation timeout and test the escalation flow.
