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
Test-NetConnection -Computername Splunk_IP -port 9997
```

---

## Splunk Verification

Verified the endpoint appeared in:
- Splunk Forwarder Management
- Connected forwarder list
- Active forwarder status

Navigation Path:
```text
Settings > Forwarder Management
```

---

## Troubleshooting Notes

If the forwarder does not appear:
- Restart SplunkForwarder Service
- Verify port 9997 connectivity
- Confirm receiving indexer IP address
- Check firewall configuration

---

## Notes

Successful verification confirmed:
- Universal Forwarder installation
- Network communication
- Centralized log forwarding functionality

## References
- [Splunk Universal Forwarder Documentation](https://docs.splunk.com/Documentation/Forwarder)
