# Windows Log Forwarding

## Objective
Configure Windows Event Log forwarding from a Windows endpoint to Splunk Enterprise using Splunk Universal Forwarder.

## Environment
- Windows 10
- Splunk Universal Forwarder
- Splunk Enterprise
- Local single-host lab environment

---

## Forwarding Workflow

1. Installed Splunk Universal Forwarder on Windows endpoint
2. Configured local receiving indexer connection (127.0.0.1:9997)
3. Enabled receiving on Splunk Enterprise port 9997
4. Created and configured `inputs.conf` for Windows Event Logs
5. Restarted SplunkForwarder service
6. Verified successful log ingestion within Splunk Search & Reporting

---

## Data Sources Forwarded

Forwarded Windows Event Logs including:
- Security Logs
- System Logs
- Application Logs

---

## Universal Forwarder Configuration

Configured Windows Event Log collection using:

```ini
[WinEventLog://Application]
disabled = 0

[WinEventLog://System]
disabled = 0

[WinEventLog://Security]
disabled = 0
