# Splunk Installation on Linux

## Objective
Install Splunk Enterprise on Ubuntu 22.04 using both GUI and CLI installation methods.

## Environment
- Ubuntu 22.04 Desktop
- Splunk Enterprise 9.0.1

---

# GUI Installation

## Installation Steps
1. Accessed the Splunk Enterprise download portal
2. Created a Splunk account
3. Downloaded the `.deb` package
4. Opened the installer using Software Install
5. Installed Splunk Enterprise
6. Verified successful installation

---

# CLI Installation

## Installation Steps
1. Downloaded Splunk package using `wget`
2. Navigated to installation directory
3. Extracted Splunk archive
4. Started Splunk service
5. Accepted Splunk license agreement
6. Configured administrator credentials

---

## Commands Used

### Extract Splunk Archive

```bash
tar xvzf splunk-9.0.1-82c987350fde-Linux-x86_64.tgz
```

### Start Splunk

```bash
/opt/splunk/bin/splunk start --accept-license
```

### Enable Boot Start

```bash
/opt/splunk/bin/splunk enable boot-start
```

### Check Splunk Status

```bash
/opt/splunk/bin/splunk status
```

---

## Verification

Verified:
- Splunk web interface accessible
- Splunk started successfully
- Boot-start configuration enabled
- Splunk status returned operational output

Web Interface:

```text
http://blueatom-VirtualBox:8000
```

---

## Notes

By default, Splunk on Linux does not automatically start during system boot until boot-start is enabled.

## References

- [Install Splunk Enterprise on Linux](https://help.splunk.com/en/splunk-enterprise/get-started/install-and-upgrade/9.1/install-splunk-enterprise-on-linux-or-macos)
