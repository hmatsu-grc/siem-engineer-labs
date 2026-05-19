# Splunk Installation on Windows

## Objective
Install Splunk Enterprise on a local Windows 11 system.

## Environment
- Windows 11
- Splunk Enterprise 9.0.0.1

## Installation Steps
1. Accessed the Splunk Enterprise download portal
2. Created a Splunk account
3. Downloaded the 64-bit MSI installer
4. Reviewed and accepted the Splunk license agreement
5. Selected custom installation options
6. Configured installation directory
7. Installed Splunk as a local system service
8. Configured administrator credentials
9. Completed installation and launched Splunk

## Verification
Verified:
- Splunk web interface accessible locally:
  - https://127.0.0.1:8000
- Splunkd Service running successfully
- Startup type configured as Automatic

## Monitoring
Reviewed Splunk service status using:
- services.msc
- Splunkd Service

## References
- [Splunk Enterprise Downloads](https://www.splunk.com/)
