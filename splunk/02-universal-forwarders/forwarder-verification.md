# Splunk Universal Forwarder Verification

## Objective
Verify successful Splunk Universal Forwarder installation and communication with the Splunk indexer.

## Verification Steps

### Service Verification

Verified the following Windows service was running:

- SplunkForwarder Service

Checked service status using:
- `services.msc`

---

## Connectivity Verification

Verified endpoint connectivity to the Splunk indexer on port 9997.

### PowerShell Command

```powershell
Test-NetConnection -ComputerName 127.0.0.1 -Port 9997
```

---

## Splunk Verification

Verified forwarder communication and Windows Event Log ingestion within Splunk Search & Reporting.

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

If the forwarder does not appear:
- Restart SplunkForwarder Service
- Verify port 9997 connectivity
- Confirm receiving indexer IP address
- Check firewall configuration

Resolved ingestion issues caused by:
- incorrect Windows file extension (`inputs.conf.txt`)
- missing `inputs.conf` configuration
- Windows hidden file extensions

---

## Notes

Successful verification confirmed:
- Universal Forwarder installation
- TCP communication over port 9997
- Centralized log forwarding functionality

## References
- [Splunk Universal Forwarder Documentation](https://docs.splunk.com/Documentation/Forwarder)
