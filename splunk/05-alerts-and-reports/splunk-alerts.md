# Splunk Alerts

## Objective

Review Splunk alert functionality for detecting and monitoring security events using scheduled and real-time searches.

---

## Alert Overview

Splunk alerts are saved searches that trigger when specified conditions are met.

Alerts can operate in:
- scheduled mode
- real-time mode

Alerts help analysts automate monitoring and identify suspicious activity without manually executing searches.

---

## Alert Configuration Workflow

### Create an Alert

Navigated to:

```text
Search & Reporting
```

Executed an SPL query and selected:

```text
Save As → Alert
```

---

## Alert Information

Configured:
- alert title
- alert description
- trigger conditions
- alert permissions

---

## Alert Types

### Scheduled Alerts

Scheduled alerts execute searches at defined intervals.

Example intervals:
- every 5 minutes
- hourly
- daily

---

### Real-Time Alerts

Real-time alerts continuously monitor incoming events.

Used for:
- active threat monitoring
- suspicious activity detection
- high-priority security events

### Notes

Excessive real-time alerts may increase Splunk server resource usage.

---

## Example Security Use Cases

Alerts can be configured for:
- failed login attempts
- brute-force activity
- malware detections
- unauthorized access attempts
- suspicious IP activity
- unusual account behavior

---

## Verification

Verified:
- alert creation workflow
- scheduled alert configuration
- real-time alert configuration
- alert visibility within Search & Reporting

---

## Notes

Splunk alerts improve:
- incident response speed
- recurring threat detection
- monitoring consistency
- analyst visibility into suspicious activity

Alerts help reduce the need for repetitive manual searches during investigations.

---

## References

- https://help.splunk.com/en/splunk-enterprise/alert-and-respond/alerting-manual
