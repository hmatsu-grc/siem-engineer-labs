# Splunk Universal Forwarder Installation

## Objective
Install and configure Splunk Universal Forwarder on a Windows endpoint for centralized log collection.

## Environment
- Windows 11
- Splunk Universal Forwarder 9.0.0.1
- Splunk Enterprise

---

## Installation Steps

1. Downloaded Splunk Universal Forwarder installer
2. Reviewed Splunk license agreement
3. Verified installer MD5 checksum
4. Selected on-premises Splunk Enterprise deployment
5. Configured local Splunk Enterprise receiver connection (`127.0.0.1:9997`)
6. Installed Universal Forwarder using default configuration
7. Completed installation and verified service startup

---

## Configuration Details

| Setting | Value |
|---|---|
| Deployment Type | On-Premises Splunk Enterprise |
| Receiving Target | 127.0.0.1:9997 |
| Forwarder Type | Universal Forwarder |

---

## Verification

Verified:
- SplunkForwarder Service running
- Universal Forwarder installation completed successfully
- Endpoint connected to Splunk indexer
- Active forward-server connection verified

---

## Commands Used

### Verify Installer MD5

```powershell
Get-FileHash .\splunkforwarder-9.0.0.1-9e907cedecb1-x64-release.msi -Algorithm md5
```

### Verify Active Forwarding Connection

```cmd
splunk list forward-server
```

---

## Notes

Configured the Universal Forwarder within a local single-host lab environment using a direct connection to Splunk Enterprise without a deployment server.

## References
- [Splunk Universal Forwarder Documentation](https://docs.splunk.com/Documentation/Forwarder)
