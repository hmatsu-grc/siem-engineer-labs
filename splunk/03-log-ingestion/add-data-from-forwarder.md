# Add Data from Forwarder

## Objective

Add Windows Event Logs to Splunk using a Splunk Universal Forwarder.

## Workflow

1. Navigated to:
```text
Settings > Add Data
```

2. Selected:
```text
Forward
```

3. Added the Windows endpoint host
4. Assigned a Server Class Name
5. Selected local Windows Event Logs for monitoring
6. Chose destination index for incoming events
7. Submitted configuration and started data search

---

## Data Sources

Configured collection for:
- Security Logs
- System Logs
- Application Logs

---

## Notes

Created a custom index named:
```text
WinLog_clients
```

Verified incoming events after receiver configuration.
