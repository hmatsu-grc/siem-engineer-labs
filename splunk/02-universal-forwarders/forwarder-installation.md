# Splunk Universal Forwarder Installation

## Objective
Install and configure Splunk Universal Forwarder on a Windows endpoint for centralized log collection.

## Environment
- Windows 10
- Splunk Universal Forwarder 9.0.0.1
- Splunk Enterprise

---

## Installation Steps

1. Downloaded Splunk Universal Forwarder installer
2. Reviewed Splunk license agreement
3. Verified installer MD5 checksum
4. Selected on-premises Splunk Enterprise deployment
5. Configured receiving indexer IP address and port
6. Installed Universal Forwarder using default configuration
7. Completed installation and verified service startup

---

## Configuration Details

| Setting | Value |
|---|---|
| Deployment Type | On-Premises Splunk Enterprise |
| Receiving Port | 9997 |
| Forwarder Type | Universal Forwarder |

---

## Verification

Verified:
- SplunkForwarder Service running
- Universal Forwarder installation completed successfully
- Endpoint connected to Splunk indexer

---

## Commands Used

### Verify Installer MD5

```powershell
Get-FileHash .\splunkforwarder-9.0.0.1-9e907cedecb1-x64-release.msi -Algorithm md5
```

---

## Notes

Configured the Universal Forwarder using default lab settings without a deployment server.

## References
- [Splunk Universal Forwarder Documentation](https://docs.splunk.com/Documentation/Forwarder)
