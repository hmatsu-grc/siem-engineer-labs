# Add Data from Forwarder

## Objective

Add Windows Event Logs to Splunk using a Splunk Universal Forwarder.

---

## Add Data Workflow

### Open Add Data

Navigated to:

```text
Settings → Add Data
```

Selected local data forwarding configuration.

---

### Select Data Sources

1. Selected local Windows Event Logs
2. Selected log sources
3. Clicked Next

---

### Configure the Index

Configured forwarding target:
```text
127.0.0.1:9997
```

Configured destination index for incoming logs.

Used default Splunk index:

```text
main
```

After submission, selected:

```text
Start Searching
```

---

## Check Indexes

Navigated to:

```text
Settings → Indexes
```

Verified forwarded Windows Event Logs were ingesting into:

```text
main
```

Initially, no incoming events were visible because the receiving port had not yet been configured.

---

## Add Receiver

Navigated to:

```text
Settings → Forwarding and Receiving
```

Added new receiving port:

```text
9997
```

Configured Splunk Enterprise to receive forwarded event data from the local Universal Forwarder on port 9997.

---

## Verification

After configuring the receiving port:
- Incoming events appeared within the index
- Forwarded Windows logs became searchable
- Verified event visibility using Search & Reporting
- Performed a basic event search to confirm successful log forwarding

Verified forwarder communication using:

```spl
index=_internal component=TcpOutputProc
```

Verified Windows Event Log ingestion using:

```spl
source="WinEventLog:*"
```

---

## Data Sources

Configured collection for:
- Security Logs
- System Logs
- Application Logs

---

## Notes

Configured forwarded Windows Event Logs to ingest into the `main` index using a local Universal Forwarder to Splunk Enterprise connection.

Verified incoming events after receiver configuration.

---

## References

- https://docs.splunk.com/Documentation/Forwarder
