# Windows Log Forwarding

## Objective
Configure Windows Event Log forwarding from a Windows endpoint to Splunk Enterprise using Splunk Universal Forwarder.

## Environment
- Windows 10
- Splunk Universal Forwarder 9.0.0.1
- Splunk Enterprise

---

## Forwarding Workflow

1. Installed Splunk Universal Forwarder on Windows endpoint
2. Configured receiving indexer IP address
3. Configured receiving port 9997
4. Enabled Windows Event Log forwarding
5. Verified log ingestion within Splunk

---

## Data Sources Forwarded

Forwarded Windows Event Logs including:
- Security Logs
- System Logs
- Application Logs

---

## Connectivity Verification

Verified communication between the endpoint and Splunk indexer using:

```powershell
Test-NetConnection -Computername Splunk_IP -port 9997
```

---

## Splunk Verification

Verified forwarded logs appeared within:
- Search & Reporting
- Forwarder Management
- Indexed event data

---

## Notes

Configured log forwarding within a lab environment using a direct indexer connection without a deployment server.

## References
- [Splunk Universal Forwarder Documentation](https://docs.splunk.com/Documentation/Forwarder)
