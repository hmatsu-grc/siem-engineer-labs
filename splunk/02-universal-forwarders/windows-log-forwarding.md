# Windows Log Forwarding

## Objective
Configure Windows Event Log forwarding from a Windows endpoint to Splunk Enterprise using Splunk Universal Forwarder.

## Environment
- Windows 11
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

## Windows Event Log Input Configuration

Configured Windows Event Log collection using:

```ini
[default]
host = windows-lab

[WinEventLog://Application]
disabled = 0
index = main

[WinEventLog://System]
disabled = 0
index = main

[WinEventLog://Security]
disabled = 0
index = main
```

## Notes

Configured Windows Event Logs to forward into the `main` index using the local Universal Forwarder configuration file (`inputs.conf`).

---

## Connectivity Verification

Verified communication between the Universal Forwarder and Splunk receiver using:

```powershell
Test-NetConnection -ComputerName 127.0.0.1 -Port 9997
```

Successful connection returned:
- `TcpTestSucceeded : True`

---

## Splunk Verification

Verified forwarded logs appeared within:
- Search & Reporting
- Indexed event data
- Internal forwarder communication logs

### Example Searches Used

Verified forwarder communication:

```spl
index=_internal component=TcpOutputProc
```

Verified Windows Event Log ingestion:

```spl
source="WinEventLog:*"
```

---

## Troubleshooting Notes

Resolved ingestion issues caused by:
- incorrect Windows file extension (`inputs.conf.txt`)
- missing `inputs.conf` configuration
- Windows hidden file extensions

Restarted `SplunkForwarder` service after configuration changes.

---

## References

- [Splunk Universal Forwarder Documentation](https://docs.splunk.com/Documentation/Forwarder)
