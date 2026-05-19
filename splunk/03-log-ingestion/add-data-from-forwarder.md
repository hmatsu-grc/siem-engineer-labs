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

Selected:

```text
Forward
```

---

### Configure the Host

1. Added the computer to the selected hosts list
2. Assigned a Server Class Name
3. Clicked Next


---

### Select Data Sources

1. Selected local Windows Event Logs
2. Selected log sources
3. Clicked Next

---

### Configure the Index

Configured destination index for incoming logs.

Created custom index:

```text
WinLog_clients
```

Steps performed:
1. Clicked Create New Index
2. Named the index 'WinLog_clients'
3. Clicked Review
4. Clicked Submit

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

Searched for index created previously:

```text
WinLog_clients
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

This port allows Splunk Universal Forwarders to send event data to the Splunk indexer.

---

## Verification

After configuring the receiving port:
- Incoming events appeared within the index
- Forwarded Windows logs became searchable
- Verified event visibility using Search & Reporting
- Performed a basic event search to confirm successful log forwarding



## Data Sources

Configured collection for:
- Security Logs
- System Logs
- Application Logs

---

## Notes

Created a custom index named:
```text
WinLog_clients
```

Verified incoming events after receiver configuration.
